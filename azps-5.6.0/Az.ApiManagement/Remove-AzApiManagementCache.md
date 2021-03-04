---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: acbcddb5a3ba9a193be52deb287ce3b169c72834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911794"
---
# <span data-ttu-id="e270a-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e270a-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="e270a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e270a-102">SYNOPSIS</span></span>
<span data-ttu-id="e270a-103">移除緩存實體。</span><span class="sxs-lookup"><span data-stu-id="e270a-103">Removes the cache entity.</span></span>

## <span data-ttu-id="e270a-104">語法</span><span class="sxs-lookup"><span data-stu-id="e270a-104">SYNTAX</span></span>

### <span data-ttu-id="e270a-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="e270a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e270a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e270a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e270a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e270a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e270a-108">描述</span><span class="sxs-lookup"><span data-stu-id="e270a-108">DESCRIPTION</span></span>
<span data-ttu-id="e270a-109">Cmdlet **Remove-AzApiManagementCache 會** 移除緩存實體。</span><span class="sxs-lookup"><span data-stu-id="e270a-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="e270a-110">例子</span><span class="sxs-lookup"><span data-stu-id="e270a-110">EXAMPLES</span></span>

### <span data-ttu-id="e270a-111">範例 1：移除 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="e270a-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="e270a-112">此 Cmdlet 會從 `centralus` Api 管理服務移除緩存。</span><span class="sxs-lookup"><span data-stu-id="e270a-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="e270a-113">參數</span><span class="sxs-lookup"><span data-stu-id="e270a-113">PARAMETERS</span></span>

### <span data-ttu-id="e270a-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="e270a-114">-CacheId</span></span>
<span data-ttu-id="e270a-115">現有 cacheId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e270a-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="e270a-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e270a-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e270a-117">-內容</span><span class="sxs-lookup"><span data-stu-id="e270a-117">-Context</span></span>
<span data-ttu-id="e270a-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e270a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e270a-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e270a-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e270a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e270a-120">-DefaultProfile</span></span>
<span data-ttu-id="e270a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e270a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e270a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e270a-122">-InputObject</span></span>
<span data-ttu-id="e270a-123">PsApiManagementCache 實例。</span><span class="sxs-lookup"><span data-stu-id="e270a-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="e270a-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e270a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e270a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e270a-125">-PassThru</span></span>
<span data-ttu-id="e270a-126">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="e270a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e270a-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="e270a-127">This parameter is optional.</span></span>
<span data-ttu-id="e270a-128">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="e270a-128">Default value is false.</span></span>

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

### <span data-ttu-id="e270a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e270a-129">-ResourceId</span></span>
<span data-ttu-id="e270a-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="e270a-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="e270a-131">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="e270a-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e270a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e270a-132">-Confirm</span></span>
<span data-ttu-id="e270a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e270a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e270a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e270a-134">-WhatIf</span></span>
<span data-ttu-id="e270a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e270a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e270a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e270a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e270a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e270a-137">CommonParameters</span></span>
<span data-ttu-id="e270a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e270a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e270a-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e270a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e270a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e270a-140">INPUTS</span></span>

### <span data-ttu-id="e270a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="e270a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e270a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e270a-142">System.String</span></span>

### <span data-ttu-id="e270a-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e270a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e270a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e270a-144">OUTPUTS</span></span>

### <span data-ttu-id="e270a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e270a-145">System.Boolean</span></span>

## <span data-ttu-id="e270a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e270a-146">NOTES</span></span>

## <span data-ttu-id="e270a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e270a-147">RELATED LINKS</span></span>

[<span data-ttu-id="e270a-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e270a-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="e270a-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e270a-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="e270a-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e270a-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
