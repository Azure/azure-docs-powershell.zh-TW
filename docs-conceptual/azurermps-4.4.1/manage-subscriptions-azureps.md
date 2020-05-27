---
title: 使用 Azure PowerShell 來管理 Azure 訂用帳戶 | Microsoft Docs
description: 使用 Azure PowerShell 來管理 Azure 訂用帳戶
keywords: Azure PowerShell, 訂用帳戶
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 921da316b1e8a57f0879c87820297de662b2cfd0
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386726"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="e2fae-104">管理多個 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="e2fae-104">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="e2fae-105">如果您是 Azure 的新手，可能只會擁有單一訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e2fae-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="e2fae-106">但是，如果您已使用 Azure 一段時間，可能已建立了多個 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="e2fae-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="e2fae-107">您可以將 Azure PowerShell 設定為針對特定訂用帳戶來執行命令。</span><span class="sxs-lookup"><span data-stu-id="e2fae-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="e2fae-108">取得您帳戶中所有訂用帳戶的清單。</span><span class="sxs-lookup"><span data-stu-id="e2fae-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="e2fae-109">預設設定。</span><span class="sxs-lookup"><span data-stu-id="e2fae-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="e2fae-110">執行 `Get-AzureRmContext` Cmdlet 來驗證變更。</span><span class="sxs-lookup"><span data-stu-id="e2fae-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="e2fae-111">一旦您設定預設訂用帳戶後，所有後續的 Azure PowerShell 命令都會對此訂用帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="e2fae-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
