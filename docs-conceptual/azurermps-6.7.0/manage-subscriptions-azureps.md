---
title: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
description: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: e1606ddb02adf1de2cb5496917d61755ac3dad23
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018806"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="00d2b-103">管理多個 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="00d2b-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="00d2b-104">如果您是 Azure 的新手，可能只會擁有單一訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="00d2b-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="00d2b-105">但是，如果您已使用 Azure 一段時間，可能已建立了多個 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="00d2b-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="00d2b-106">您可以將 Azure PowerShell 設定為針對特定訂用帳戶來執行命令。</span><span class="sxs-lookup"><span data-stu-id="00d2b-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="00d2b-107">取得您帳戶中所有訂用帳戶的清單。</span><span class="sxs-lookup"><span data-stu-id="00d2b-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="00d2b-108">預設設定。</span><span class="sxs-lookup"><span data-stu-id="00d2b-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="00d2b-109">執行 `Get-AzureRmContext` Cmdlet 來驗證變更。</span><span class="sxs-lookup"><span data-stu-id="00d2b-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="00d2b-110">一旦您設定預設訂用帳戶後，所有後續的 Azure PowerShell 命令都會對此訂用帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="00d2b-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
