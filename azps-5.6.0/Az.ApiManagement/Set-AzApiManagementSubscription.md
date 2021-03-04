---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: aea1b80507b753a84afd9228c4845da973273a37
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908669"
---
# <span data-ttu-id="0a45c-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a45c-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="0a45c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a45c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a45c-103">設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a45c-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="0a45c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a45c-104">SYNTAX</span></span>

### <span data-ttu-id="0a45c-105">ByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0a45c-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45c-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="0a45c-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a45c-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a45c-107">DESCRIPTION</span></span>
<span data-ttu-id="0a45c-108">**Set-AzApiManagementSubscription** Cmdlet 會設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a45c-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="0a45c-109">例子</span><span class="sxs-lookup"><span data-stu-id="0a45c-109">EXAMPLES</span></span>

### <span data-ttu-id="0a45c-110">範例 1：設定訂閱的狀態和主要及次要金鑰</span><span class="sxs-lookup"><span data-stu-id="0a45c-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="0a45c-111">此命令會設定訂閱的主鍵和次要鍵，並啟用它。</span><span class="sxs-lookup"><span data-stu-id="0a45c-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="0a45c-112">參數</span><span class="sxs-lookup"><span data-stu-id="0a45c-112">PARAMETERS</span></span>

### <span data-ttu-id="0a45c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="0a45c-113">-Context</span></span>
<span data-ttu-id="0a45c-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0a45c-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a45c-115">-DefaultProfile</span></span>
<span data-ttu-id="0a45c-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a45c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="0a45c-117">-ExpiresOn</span></span>
<span data-ttu-id="0a45c-118">指定訂閱到期日。</span><span class="sxs-lookup"><span data-stu-id="0a45c-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="0a45c-119">此參數的預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="0a45c-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a45c-120">-InputObject</span></span>
<span data-ttu-id="0a45c-121">PsApiManagementSubscription 的實例。</span><span class="sxs-lookup"><span data-stu-id="0a45c-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="0a45c-122">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="0a45c-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a45c-123">-Name</span></span>
<span data-ttu-id="0a45c-124">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="0a45c-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a45c-125">-PassThru</span></span>
<span data-ttu-id="0a45c-126">Passthru</span><span class="sxs-lookup"><span data-stu-id="0a45c-126">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0a45c-127">-PrimaryKey</span></span>
<span data-ttu-id="0a45c-128">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="0a45c-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="0a45c-129">如果沒有指定，系統會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="0a45c-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0a45c-130">此參數必須長 1 到 300 個字元。</span><span class="sxs-lookup"><span data-stu-id="0a45c-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-131">-範圍</span><span class="sxs-lookup"><span data-stu-id="0a45c-131">-Scope</span></span>
<span data-ttu-id="0a45c-132">訂閱的範圍，無論是 Api 範圍 /apis/{apiId} 或產品範圍 /products/{productId} 或全域 API 範圍 /apis 或全域範圍 /。</span><span class="sxs-lookup"><span data-stu-id="0a45c-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="0a45c-133">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="0a45c-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0a45c-134">-SecondaryKey</span></span>
<span data-ttu-id="0a45c-135">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="0a45c-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="0a45c-136">如果沒有指定，系統會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="0a45c-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="0a45c-137">此參數必須長 1 到 300 個字元。</span><span class="sxs-lookup"><span data-stu-id="0a45c-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-138">-State</span><span class="sxs-lookup"><span data-stu-id="0a45c-138">-State</span></span>
<span data-ttu-id="0a45c-139">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="0a45c-139">Specifies the subscription state.</span></span>
<span data-ttu-id="0a45c-140">此參數的預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="0a45c-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="0a45c-141">-StateComment</span></span>
<span data-ttu-id="0a45c-142">指定訂閱狀態批註。</span><span class="sxs-lookup"><span data-stu-id="0a45c-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="0a45c-143">此參數的預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="0a45c-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a45c-144">-SubscriptionId</span></span>
<span data-ttu-id="0a45c-145">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a45c-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="0a45c-146">-UserId</span></span>
<span data-ttu-id="0a45c-147">訂閱的擁有者。</span><span class="sxs-lookup"><span data-stu-id="0a45c-147">The owner of the subscription.</span></span> <span data-ttu-id="0a45c-148">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="0a45c-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="0a45c-149">-Confirm</span></span>
<span data-ttu-id="0a45c-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a45c-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a45c-151">-WhatIf</span></span>
<span data-ttu-id="0a45c-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a45c-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a45c-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a45c-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a45c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a45c-154">CommonParameters</span></span>
<span data-ttu-id="0a45c-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a45c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a45c-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a45c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a45c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="0a45c-157">INPUTS</span></span>

### <span data-ttu-id="0a45c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="0a45c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a45c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="0a45c-159">System.String</span></span>

### <span data-ttu-id="0a45c-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0a45c-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0a45c-161">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a45c-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0a45c-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a45c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a45c-163">輸出</span><span class="sxs-lookup"><span data-stu-id="0a45c-163">OUTPUTS</span></span>

### <span data-ttu-id="0a45c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a45c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="0a45c-165">筆記</span><span class="sxs-lookup"><span data-stu-id="0a45c-165">NOTES</span></span>

## <span data-ttu-id="0a45c-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a45c-166">RELATED LINKS</span></span>

[<span data-ttu-id="0a45c-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a45c-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="0a45c-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a45c-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="0a45c-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a45c-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


