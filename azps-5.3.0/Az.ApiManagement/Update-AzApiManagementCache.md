---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287603"
---
# <span data-ttu-id="71dda-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71dda-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="71dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71dda-102">SYNOPSIS</span></span>
<span data-ttu-id="71dda-103">更新 Api 管理服務中的快取。</span><span class="sxs-lookup"><span data-stu-id="71dda-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="71dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="71dda-104">SYNTAX</span></span>

### <span data-ttu-id="71dda-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="71dda-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71dda-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71dda-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71dda-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71dda-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71dda-108">說明</span><span class="sxs-lookup"><span data-stu-id="71dda-108">DESCRIPTION</span></span>
<span data-ttu-id="71dda-109">Cmdlet **更新-AzApiManagementCache** 會更新 ApiManagement 服務中的快取。</span><span class="sxs-lookup"><span data-stu-id="71dda-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="71dda-110">示例</span><span class="sxs-lookup"><span data-stu-id="71dda-110">EXAMPLES</span></span>

### <span data-ttu-id="71dda-111">範例1：在 centralus 中更新快取的描述</span><span class="sxs-lookup"><span data-stu-id="71dda-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="71dda-112">在美國中部更新快取的描述。</span><span class="sxs-lookup"><span data-stu-id="71dda-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="71dda-113">參數</span><span class="sxs-lookup"><span data-stu-id="71dda-113">PARAMETERS</span></span>

### <span data-ttu-id="71dda-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="71dda-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="71dda-115">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71dda-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="71dda-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71dda-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="71dda-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="71dda-117">-CacheId</span></span>
<span data-ttu-id="71dda-118">新快取的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71dda-118">Identifier of new cache.</span></span>
<span data-ttu-id="71dda-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71dda-119">This parameter is required.</span></span>

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

### <span data-ttu-id="71dda-120">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="71dda-120">-ConnectionString</span></span>
<span data-ttu-id="71dda-121">Redis [連接字串]。</span><span class="sxs-lookup"><span data-stu-id="71dda-121">Redis Connection String.</span></span>
<span data-ttu-id="71dda-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71dda-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="71dda-123">-內容</span><span class="sxs-lookup"><span data-stu-id="71dda-123">-Context</span></span>
<span data-ttu-id="71dda-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="71dda-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="71dda-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71dda-125">This parameter is required.</span></span>

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

### <span data-ttu-id="71dda-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71dda-126">-DefaultProfile</span></span>
<span data-ttu-id="71dda-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71dda-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71dda-128">-描述</span><span class="sxs-lookup"><span data-stu-id="71dda-128">-Description</span></span>
<span data-ttu-id="71dda-129">快取說明。</span><span class="sxs-lookup"><span data-stu-id="71dda-129">Cache Description.</span></span>
<span data-ttu-id="71dda-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71dda-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="71dda-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71dda-131">-InputObject</span></span>
<span data-ttu-id="71dda-132">PsApiManagementCache 的實例。</span><span class="sxs-lookup"><span data-stu-id="71dda-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="71dda-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71dda-133">This parameter is required.</span></span>

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

### <span data-ttu-id="71dda-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71dda-134">-PassThru</span></span>
<span data-ttu-id="71dda-135">如果已指定，則 ServiceManagement 的 ApiManagement 實例，代表修改過的快取的 PsApiManagementCache 類型將會寫入輸出中。</span><span class="sxs-lookup"><span data-stu-id="71dda-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="71dda-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71dda-136">-ResourceId</span></span>
<span data-ttu-id="71dda-137">[快取] 的 [Arm] ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71dda-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="71dda-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71dda-138">This parameter is required.</span></span>

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

### <span data-ttu-id="71dda-139">-確認</span><span class="sxs-lookup"><span data-stu-id="71dda-139">-Confirm</span></span>
<span data-ttu-id="71dda-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71dda-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71dda-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71dda-141">-WhatIf</span></span>
<span data-ttu-id="71dda-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71dda-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71dda-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71dda-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71dda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71dda-144">CommonParameters</span></span>
<span data-ttu-id="71dda-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71dda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71dda-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71dda-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71dda-147">輸入</span><span class="sxs-lookup"><span data-stu-id="71dda-147">INPUTS</span></span>

### <span data-ttu-id="71dda-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="71dda-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="71dda-149">System.object</span><span class="sxs-lookup"><span data-stu-id="71dda-149">System.String</span></span>

### <span data-ttu-id="71dda-150">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="71dda-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="71dda-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="71dda-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71dda-152">輸出</span><span class="sxs-lookup"><span data-stu-id="71dda-152">OUTPUTS</span></span>

### <span data-ttu-id="71dda-153">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="71dda-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="71dda-154">筆記</span><span class="sxs-lookup"><span data-stu-id="71dda-154">NOTES</span></span>

## <span data-ttu-id="71dda-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="71dda-155">RELATED LINKS</span></span>

[<span data-ttu-id="71dda-156">新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71dda-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="71dda-157">AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71dda-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="71dda-158">移除-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="71dda-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
