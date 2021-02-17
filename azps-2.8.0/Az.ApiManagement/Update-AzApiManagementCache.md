---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: c8c535168a86607daab27ab89340d231bb4e4bd3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406888"
---
# <span data-ttu-id="71fc7-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="71fc7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="71fc7-103">更新 Api 管理服務中的緩存。</span><span class="sxs-lookup"><span data-stu-id="71fc7-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="71fc7-104">語法</span><span class="sxs-lookup"><span data-stu-id="71fc7-104">SYNTAX</span></span>

### <span data-ttu-id="71fc7-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="71fc7-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71fc7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71fc7-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71fc7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71fc7-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71fc7-108">描述</span><span class="sxs-lookup"><span data-stu-id="71fc7-108">DESCRIPTION</span></span>
<span data-ttu-id="71fc7-109">Cmdlet **Update-AzApiManagementCache 會** 更新 ApiManagement 服務中的快訊。</span><span class="sxs-lookup"><span data-stu-id="71fc7-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="71fc7-110">例子</span><span class="sxs-lookup"><span data-stu-id="71fc7-110">EXAMPLES</span></span>

### <span data-ttu-id="71fc7-111">範例 1：更新 centralus 中的 Cache 描述</span><span class="sxs-lookup"><span data-stu-id="71fc7-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="71fc7-112">更新美國中地區之 Cache 的描述。</span><span class="sxs-lookup"><span data-stu-id="71fc7-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="71fc7-113">參數</span><span class="sxs-lookup"><span data-stu-id="71fc7-113">PARAMETERS</span></span>

### <span data-ttu-id="71fc7-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="71fc7-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="71fc7-115">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71fc7-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="71fc7-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="71fc7-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fc7-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="71fc7-117">-CacheId</span></span>
<span data-ttu-id="71fc7-118">新緩存的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71fc7-118">Identifier of new cache.</span></span>
<span data-ttu-id="71fc7-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="71fc7-119">This parameter is required.</span></span>

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

### <span data-ttu-id="71fc7-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="71fc7-120">-ConnectionString</span></span>
<span data-ttu-id="71fc7-121">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="71fc7-121">Redis Connection String.</span></span>
<span data-ttu-id="71fc7-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="71fc7-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fc7-123">-內容</span><span class="sxs-lookup"><span data-stu-id="71fc7-123">-Context</span></span>
<span data-ttu-id="71fc7-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="71fc7-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="71fc7-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="71fc7-125">This parameter is required.</span></span>

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

### <span data-ttu-id="71fc7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fc7-126">-DefaultProfile</span></span>
<span data-ttu-id="71fc7-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="71fc7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71fc7-128">-描述</span><span class="sxs-lookup"><span data-stu-id="71fc7-128">-Description</span></span>
<span data-ttu-id="71fc7-129">緩存描述。</span><span class="sxs-lookup"><span data-stu-id="71fc7-129">Cache Description.</span></span>
<span data-ttu-id="71fc7-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="71fc7-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fc7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71fc7-131">-InputObject</span></span>
<span data-ttu-id="71fc7-132">PsApiManagementCache 實例。</span><span class="sxs-lookup"><span data-stu-id="71fc7-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="71fc7-133">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="71fc7-133">This parameter is required.</span></span>

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

### <span data-ttu-id="71fc7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71fc7-134">-PassThru</span></span>
<span data-ttu-id="71fc7-135">如果指定，代表已修改之緩存的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache 類型實例就會寫入輸出。</span><span class="sxs-lookup"><span data-stu-id="71fc7-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="71fc7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71fc7-136">-ResourceId</span></span>
<span data-ttu-id="71fc7-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="71fc7-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="71fc7-138">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="71fc7-138">This parameter is required.</span></span>

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

### <span data-ttu-id="71fc7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="71fc7-139">-Confirm</span></span>
<span data-ttu-id="71fc7-140">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="71fc7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71fc7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fc7-141">-WhatIf</span></span>
<span data-ttu-id="71fc7-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71fc7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71fc7-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71fc7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71fc7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fc7-144">CommonParameters</span></span>
<span data-ttu-id="71fc7-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71fc7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fc7-146">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71fc7-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fc7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="71fc7-147">INPUTS</span></span>

### <span data-ttu-id="71fc7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="71fc7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="71fc7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="71fc7-149">System.String</span></span>

### <span data-ttu-id="71fc7-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="71fc7-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71fc7-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71fc7-152">輸出</span><span class="sxs-lookup"><span data-stu-id="71fc7-152">OUTPUTS</span></span>

### <span data-ttu-id="71fc7-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="71fc7-154">筆記</span><span class="sxs-lookup"><span data-stu-id="71fc7-154">NOTES</span></span>

## <span data-ttu-id="71fc7-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="71fc7-155">RELATED LINKS</span></span>

[<span data-ttu-id="71fc7-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="71fc7-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="71fc7-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71fc7-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
