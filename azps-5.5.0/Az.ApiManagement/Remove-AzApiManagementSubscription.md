---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128034"
---
# <span data-ttu-id="ebf47-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ebf47-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ebf47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebf47-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf47-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebf47-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="ebf47-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebf47-104">SYNTAX</span></span>

### <span data-ttu-id="ebf47-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ebf47-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf47-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ebf47-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf47-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf47-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebf47-108">說明</span><span class="sxs-lookup"><span data-stu-id="ebf47-108">DESCRIPTION</span></span>
<span data-ttu-id="ebf47-109">AzApiManagementSubscription Cmdlet 會刪除現有 **的** 訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebf47-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="ebf47-110">示例</span><span class="sxs-lookup"><span data-stu-id="ebf47-110">EXAMPLES</span></span>

### <span data-ttu-id="ebf47-111">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="ebf47-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="ebf47-112">這個命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebf47-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="ebf47-113">參數</span><span class="sxs-lookup"><span data-stu-id="ebf47-113">PARAMETERS</span></span>

### <span data-ttu-id="ebf47-114">-內容</span><span class="sxs-lookup"><span data-stu-id="ebf47-114">-Context</span></span>
<span data-ttu-id="ebf47-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebf47-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf47-116">-DefaultProfile</span></span>
<span data-ttu-id="ebf47-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebf47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf47-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebf47-118">-InputObject</span></span>
<span data-ttu-id="ebf47-119">PsApiManagementSubscription 的實例。</span><span class="sxs-lookup"><span data-stu-id="ebf47-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="ebf47-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ebf47-120">This parameter is required.</span></span>

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

### <span data-ttu-id="ebf47-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebf47-121">-PassThru</span></span>
<span data-ttu-id="ebf47-122">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $false 的值。</span><span class="sxs-lookup"><span data-stu-id="ebf47-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="ebf47-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf47-123">-ResourceId</span></span>
<span data-ttu-id="ebf47-124">訂閱的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ebf47-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="ebf47-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ebf47-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf47-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebf47-126">-SubscriptionId</span></span>
<span data-ttu-id="ebf47-127">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf47-127">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf47-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ebf47-128">-Confirm</span></span>
<span data-ttu-id="ebf47-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebf47-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf47-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf47-130">-WhatIf</span></span>
<span data-ttu-id="ebf47-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebf47-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf47-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebf47-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf47-133">CommonParameters</span></span>
<span data-ttu-id="ebf47-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebf47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf47-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ebf47-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf47-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ebf47-136">INPUTS</span></span>

### <span data-ttu-id="ebf47-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ebf47-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ebf47-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ebf47-138">System.String</span></span>

### <span data-ttu-id="ebf47-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ebf47-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ebf47-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ebf47-140">OUTPUTS</span></span>

### <span data-ttu-id="ebf47-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ebf47-141">System.Boolean</span></span>

## <span data-ttu-id="ebf47-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ebf47-142">NOTES</span></span>

## <span data-ttu-id="ebf47-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebf47-143">RELATED LINKS</span></span>

[<span data-ttu-id="ebf47-144">AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ebf47-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ebf47-145">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ebf47-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ebf47-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ebf47-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


