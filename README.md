# API-Penbet Código da Bola
extends RigidBody3D

func _ready():
	pass

func _input(event):
	if event.is_action_pressed("clique_esquerdo"):
		var camera = get_viewport().get_camera_3d()
		var direcao = (camera.global_transform.origin - global_transform.origin).normalized()
		apply_central_impulse(-direcao * 10)
