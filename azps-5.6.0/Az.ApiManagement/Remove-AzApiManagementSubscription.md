---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 1a9c44bf88e3e6aba9fdc74e588ca8e8bb7ae792
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912121"
---
# <span data-ttu-id="d1233-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1233-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="d1233-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1233-102">SYNOPSIS</span></span>
<span data-ttu-id="d1233-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1233-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="d1233-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1233-104">SYNTAX</span></span>

### <span data-ttu-id="d1233-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="d1233-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1233-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1233-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1233-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1233-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1233-108">描述</span><span class="sxs-lookup"><span data-stu-id="d1233-108">DESCRIPTION</span></span>
<span data-ttu-id="d1233-109">**Remove-AzApiManagementSubscription** Cmdlet 會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1233-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="d1233-110">例子</span><span class="sxs-lookup"><span data-stu-id="d1233-110">EXAMPLES</span></span>

### <span data-ttu-id="d1233-111">範例 1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="d1233-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="d1233-112">此命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1233-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="d1233-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1233-113">PARAMETERS</span></span>

### <span data-ttu-id="d1233-114">-內容</span><span class="sxs-lookup"><span data-stu-id="d1233-114">-Context</span></span>
<span data-ttu-id="d1233-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="d1233-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1233-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1233-116">-DefaultProfile</span></span>
<span data-ttu-id="d1233-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1233-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1233-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1233-118">-InputObject</span></span>
<span data-ttu-id="d1233-119">PsApiManagementSubscription 的實例。</span><span class="sxs-lookup"><span data-stu-id="d1233-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="d1233-120">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="d1233-120">This parameter is required.</span></span>

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

### <span data-ttu-id="d1233-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1233-121">-PassThru</span></span>
<span data-ttu-id="d1233-122">表示此 Cmdlet 會$True值 ，否則會$false值。</span><span class="sxs-lookup"><span data-stu-id="d1233-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="d1233-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1233-123">-ResourceId</span></span>
<span data-ttu-id="d1233-124">訂閱的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="d1233-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="d1233-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="d1233-125">This parameter is required.</span></span>

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

### <span data-ttu-id="d1233-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1233-126">-SubscriptionId</span></span>
<span data-ttu-id="d1233-127">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1233-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="d1233-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d1233-128">-Confirm</span></span>
<span data-ttu-id="d1233-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1233-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1233-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1233-130">-WhatIf</span></span>
<span data-ttu-id="d1233-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1233-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1233-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1233-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1233-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1233-133">CommonParameters</span></span>
<span data-ttu-id="d1233-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1233-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1233-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1233-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1233-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d1233-136">INPUTS</span></span>

### <span data-ttu-id="d1233-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="d1233-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1233-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d1233-138">System.String</span></span>

### <span data-ttu-id="d1233-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1233-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1233-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d1233-140">OUTPUTS</span></span>

### <span data-ttu-id="d1233-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1233-141">System.Boolean</span></span>

## <span data-ttu-id="d1233-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d1233-142">NOTES</span></span>

## <span data-ttu-id="d1233-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1233-143">RELATED LINKS</span></span>

[<span data-ttu-id="d1233-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1233-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="d1233-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1233-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="d1233-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1233-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


