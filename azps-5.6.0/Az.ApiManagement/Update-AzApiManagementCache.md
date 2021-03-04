---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 8c7b423090de10ea1573d268dcc3c301ec4b206d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914941"
---
# <span data-ttu-id="63c40-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="63c40-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63c40-102">SYNOPSIS</span></span>
<span data-ttu-id="63c40-103">更新 Api 管理服務中的緩存。</span><span class="sxs-lookup"><span data-stu-id="63c40-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="63c40-104">語法</span><span class="sxs-lookup"><span data-stu-id="63c40-104">SYNTAX</span></span>

### <span data-ttu-id="63c40-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="63c40-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63c40-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="63c40-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63c40-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63c40-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63c40-108">描述</span><span class="sxs-lookup"><span data-stu-id="63c40-108">DESCRIPTION</span></span>
<span data-ttu-id="63c40-109">Cmdlet **Update-AzApiManagementCache 會** 更新 ApiManagement 服務中的快訊。</span><span class="sxs-lookup"><span data-stu-id="63c40-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="63c40-110">例子</span><span class="sxs-lookup"><span data-stu-id="63c40-110">EXAMPLES</span></span>

### <span data-ttu-id="63c40-111">範例 1：更新 centralus 中的 Cache 描述</span><span class="sxs-lookup"><span data-stu-id="63c40-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="63c40-112">更新美國中部的 Cache 描述。</span><span class="sxs-lookup"><span data-stu-id="63c40-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="63c40-113">參數</span><span class="sxs-lookup"><span data-stu-id="63c40-113">PARAMETERS</span></span>

### <span data-ttu-id="63c40-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="63c40-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="63c40-115">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="63c40-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="63c40-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="63c40-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="63c40-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="63c40-117">-CacheId</span></span>
<span data-ttu-id="63c40-118">新緩存的識別碼。</span><span class="sxs-lookup"><span data-stu-id="63c40-118">Identifier of new cache.</span></span>
<span data-ttu-id="63c40-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="63c40-119">This parameter is required.</span></span>

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

### <span data-ttu-id="63c40-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="63c40-120">-ConnectionString</span></span>
<span data-ttu-id="63c40-121">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="63c40-121">Redis Connection String.</span></span>
<span data-ttu-id="63c40-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="63c40-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="63c40-123">-內容</span><span class="sxs-lookup"><span data-stu-id="63c40-123">-Context</span></span>
<span data-ttu-id="63c40-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="63c40-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="63c40-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="63c40-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63c40-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c40-126">-DefaultProfile</span></span>
<span data-ttu-id="63c40-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63c40-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63c40-128">-描述</span><span class="sxs-lookup"><span data-stu-id="63c40-128">-Description</span></span>
<span data-ttu-id="63c40-129">緩存描述。</span><span class="sxs-lookup"><span data-stu-id="63c40-129">Cache Description.</span></span>
<span data-ttu-id="63c40-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="63c40-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="63c40-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63c40-131">-InputObject</span></span>
<span data-ttu-id="63c40-132">PsApiManagementCache 實例。</span><span class="sxs-lookup"><span data-stu-id="63c40-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="63c40-133">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="63c40-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63c40-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63c40-134">-PassThru</span></span>
<span data-ttu-id="63c40-135">如果指定，代表已修改之緩存的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache 類型實例就會寫入輸出。</span><span class="sxs-lookup"><span data-stu-id="63c40-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="63c40-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63c40-136">-ResourceId</span></span>
<span data-ttu-id="63c40-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="63c40-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="63c40-138">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="63c40-138">This parameter is required.</span></span>

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

### <span data-ttu-id="63c40-139">-確認</span><span class="sxs-lookup"><span data-stu-id="63c40-139">-Confirm</span></span>
<span data-ttu-id="63c40-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63c40-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63c40-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63c40-141">-WhatIf</span></span>
<span data-ttu-id="63c40-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63c40-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63c40-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63c40-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63c40-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c40-144">CommonParameters</span></span>
<span data-ttu-id="63c40-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63c40-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c40-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63c40-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c40-147">輸入</span><span class="sxs-lookup"><span data-stu-id="63c40-147">INPUTS</span></span>

### <span data-ttu-id="63c40-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="63c40-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63c40-149">System.String</span><span class="sxs-lookup"><span data-stu-id="63c40-149">System.String</span></span>

### <span data-ttu-id="63c40-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="63c40-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63c40-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63c40-152">輸出</span><span class="sxs-lookup"><span data-stu-id="63c40-152">OUTPUTS</span></span>

### <span data-ttu-id="63c40-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="63c40-154">筆記</span><span class="sxs-lookup"><span data-stu-id="63c40-154">NOTES</span></span>

## <span data-ttu-id="63c40-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="63c40-155">RELATED LINKS</span></span>

[<span data-ttu-id="63c40-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="63c40-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="63c40-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="63c40-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
