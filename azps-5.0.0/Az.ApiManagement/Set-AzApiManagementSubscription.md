---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141167"
---
# <span data-ttu-id="c845c-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c845c-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="c845c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c845c-102">SYNOPSIS</span></span>
<span data-ttu-id="c845c-103">設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c845c-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="c845c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c845c-104">SYNTAX</span></span>

### <span data-ttu-id="c845c-105">ByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c845c-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c845c-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="c845c-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c845c-107">說明</span><span class="sxs-lookup"><span data-stu-id="c845c-107">DESCRIPTION</span></span>
<span data-ttu-id="c845c-108">**AzApiManagementSubscription** Cmdlet 會設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c845c-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="c845c-109">示例</span><span class="sxs-lookup"><span data-stu-id="c845c-109">EXAMPLES</span></span>

### <span data-ttu-id="c845c-110">範例1：設定訂閱的狀態與主要和次要金鑰</span><span class="sxs-lookup"><span data-stu-id="c845c-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="c845c-111">這個命令會設定訂閱的主要和次要金鑰，並啟用。</span><span class="sxs-lookup"><span data-stu-id="c845c-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="c845c-112">參數</span><span class="sxs-lookup"><span data-stu-id="c845c-112">PARAMETERS</span></span>

### <span data-ttu-id="c845c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="c845c-113">-Context</span></span>
<span data-ttu-id="c845c-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="c845c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c845c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c845c-115">-DefaultProfile</span></span>
<span data-ttu-id="c845c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c845c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c845c-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="c845c-117">-ExpiresOn</span></span>
<span data-ttu-id="c845c-118">指定訂閱到期日。</span><span class="sxs-lookup"><span data-stu-id="c845c-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="c845c-119">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c845c-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c845c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c845c-120">-InputObject</span></span>
<span data-ttu-id="c845c-121">PsApiManagementSubscription 的實例。</span><span class="sxs-lookup"><span data-stu-id="c845c-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="c845c-122">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c845c-122">This parameter is required.</span></span>

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

### <span data-ttu-id="c845c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c845c-123">-Name</span></span>
<span data-ttu-id="c845c-124">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="c845c-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="c845c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c845c-125">-PassThru</span></span>
<span data-ttu-id="c845c-126">passthru</span><span class="sxs-lookup"><span data-stu-id="c845c-126">passthru</span></span>

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

### <span data-ttu-id="c845c-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c845c-127">-PrimaryKey</span></span>
<span data-ttu-id="c845c-128">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="c845c-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c845c-129">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="c845c-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c845c-130">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="c845c-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c845c-131">-範圍</span><span class="sxs-lookup"><span data-stu-id="c845c-131">-Scope</span></span>
<span data-ttu-id="c845c-132">訂閱的範圍（無論是 Api 範圍/apis/{apiId} 或產品範圍/products/{productId}），還是全域 API 範圍/apis 或全域作用中。</span><span class="sxs-lookup"><span data-stu-id="c845c-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="c845c-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c845c-133">This parameter is required.</span></span>

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

### <span data-ttu-id="c845c-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c845c-134">-SecondaryKey</span></span>
<span data-ttu-id="c845c-135">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="c845c-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c845c-136">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="c845c-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c845c-137">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="c845c-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c845c-138">-State</span><span class="sxs-lookup"><span data-stu-id="c845c-138">-State</span></span>
<span data-ttu-id="c845c-139">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="c845c-139">Specifies the subscription state.</span></span>
<span data-ttu-id="c845c-140">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c845c-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c845c-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="c845c-141">-StateComment</span></span>
<span data-ttu-id="c845c-142">指定訂閱狀態批註。</span><span class="sxs-lookup"><span data-stu-id="c845c-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="c845c-143">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c845c-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c845c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c845c-144">-SubscriptionId</span></span>
<span data-ttu-id="c845c-145">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c845c-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="c845c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="c845c-146">-UserId</span></span>
<span data-ttu-id="c845c-147">訂閱的擁有者。</span><span class="sxs-lookup"><span data-stu-id="c845c-147">The owner of the subscription.</span></span> <span data-ttu-id="c845c-148">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="c845c-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="c845c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="c845c-149">-Confirm</span></span>
<span data-ttu-id="c845c-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c845c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c845c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c845c-151">-WhatIf</span></span>
<span data-ttu-id="c845c-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c845c-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c845c-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c845c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c845c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c845c-154">CommonParameters</span></span>
<span data-ttu-id="c845c-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c845c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c845c-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c845c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c845c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="c845c-157">INPUTS</span></span>

### <span data-ttu-id="c845c-158">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c845c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c845c-159">System.object</span><span class="sxs-lookup"><span data-stu-id="c845c-159">System.String</span></span>

### <span data-ttu-id="c845c-160">ApiManagement 為 Nullable "1 [PsApiManagementSubscriptionState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="c845c-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c845c-161">System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c845c-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c845c-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="c845c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c845c-163">輸出</span><span class="sxs-lookup"><span data-stu-id="c845c-163">OUTPUTS</span></span>

### <span data-ttu-id="c845c-164">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c845c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c845c-165">筆記</span><span class="sxs-lookup"><span data-stu-id="c845c-165">NOTES</span></span>

## <span data-ttu-id="c845c-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="c845c-166">RELATED LINKS</span></span>

[<span data-ttu-id="c845c-167">AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c845c-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="c845c-168">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c845c-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c845c-169">移除-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c845c-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

