Summary
=======

.. code-block:: yaml

    sylius_promotion:
        # The driver used for persistence layer.
        driver: ~
        classes:
            promotion_subject:
                model: ~
            promotion:
                model:      Sylius\Component\Promotion\Model\Promotion
                interface:  Sylius\Component\Promotion\Model\PromotionInterface
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~
                factory:    Sylius\Component\Resource\Factory\Factory
                form:
                    default: Sylius\Bundle\PromotionBundle\Form\Type\PromotionType
                    choice:  Sylius\Bundle\ResourceBundle\Form\Type\ResourceChoiceType
                validation_groups:
                    default: [ sylius ]
            promotion_rule:
                model:      Sylius\Component\Promotion\Model\Rule
                interface:  Sylius\Component\Promotion\Model\RuleInterface
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~
                factory:    Sylius\Component\Resource\Factory\Factory
                form:
                    default: Sylius\Bundle\PromotionBundle\Form\Type\RuleType
                validation_groups:
                    default: [ sylius ]
            promotion_action:
                model:      Sylius\Component\Promotion\Model\Action
                interface:  Sylius\Component\Promotion\Model\ActionInterface
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~
                factory:    Sylius\Component\Resource\Factory\Factory
                form:
                    default: Sylius\Bundle\PromotionBundle\Form\Type\ActionType
                validation_groups:
                    default: [ sylius ]
            promotion_coupon:
                model:      Sylius\Component\Promotion\Model\Coupon
                interface:  Sylius\Component\Promotion\Model\CouponInterface
                controller: Sylius\Bundle\PromotionBundle\Controller\CouponController
                repository: ~
                factory:    Sylius\Component\Resource\Factory\Factory
                form:
                    default: Sylius\Bundle\PromotionsBundle\Form\Type\CouponType
                validation_groups:
                    default: [ sylius ]
        validation_groups:
            promotion_rule_item_total_configuration: [sylius]
            promotion_rule_item_count_configuration: [sylius]
            promotion_rule_user_loyality_configuration: [sylius]
            promotion_rule_shipping_country_configuration: [sylius]
            promotion_rule_taxonomy_configuration: [sylius]
            promotion_rule_nth_order_configuration: [sylius]
            promotion_action_fixed_discount_configuration: [sylius]
            promotion_action_percentage_discount_configuration: [sylius]
            promotion_action_add_product_configuration: [sylius]
            promotion_coupon_generate_instruction: [sylius]
            promotion_action_shipping_discount_configuration: [sylius]


`phpspec2 <http://phpspec.net>`_ examples
-----------------------------------------

.. code-block:: bash

    $ composer install --dev --prefer-dist
    $ bin/phpspec run -fpretty --verbose

Bug tracking
------------

This bundle uses `GitHub issues <https://github.com/Sylius/Sylius/issues>`_.
If you have found bug, please create an issue.
