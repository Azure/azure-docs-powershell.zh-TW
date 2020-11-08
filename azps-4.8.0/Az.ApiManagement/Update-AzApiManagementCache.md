---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129684"
---
# <span data-ttu-id="67ff3-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67ff3-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="67ff3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="67ff3-103">更新 Api 管理服務中的快取。</span><span class="sxs-lookup"><span data-stu-id="67ff3-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="67ff3-104">句法</span><span class="sxs-lookup"><span data-stu-id="67ff3-104">SYNTAX</span></span>

### <span data-ttu-id="67ff3-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="67ff3-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ff3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67ff3-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ff3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67ff3-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67ff3-108">說明</span><span class="sxs-lookup"><span data-stu-id="67ff3-108">DESCRIPTION</span></span>
<span data-ttu-id="67ff3-109">Cmdlet **更新-AzApiManagementCache** 會更新 ApiManagement 服務中的快取。</span><span class="sxs-lookup"><span data-stu-id="67ff3-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="67ff3-110">示例</span><span class="sxs-lookup"><span data-stu-id="67ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="67ff3-111">範例1：在 centralus 中更新快取的描述</span><span class="sxs-lookup"><span data-stu-id="67ff3-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="67ff3-112">在美國中部更新快取的描述。</span><span class="sxs-lookup"><span data-stu-id="67ff3-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="67ff3-113">參數</span><span class="sxs-lookup"><span data-stu-id="67ff3-113">PARAMETERS</span></span>

### <span data-ttu-id="67ff3-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="67ff3-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="67ff3-115">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="67ff3-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="67ff3-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="67ff3-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="67ff3-117">-CacheId</span></span>
<span data-ttu-id="67ff3-118">新快取的識別碼。</span><span class="sxs-lookup"><span data-stu-id="67ff3-118">Identifier of new cache.</span></span>
<span data-ttu-id="67ff3-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-119">This parameter is required.</span></span>

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

### <span data-ttu-id="67ff3-120">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="67ff3-120">-ConnectionString</span></span>
<span data-ttu-id="67ff3-121">Redis [連接字串]。</span><span class="sxs-lookup"><span data-stu-id="67ff3-121">Redis Connection String.</span></span>
<span data-ttu-id="67ff3-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="67ff3-123">-內容</span><span class="sxs-lookup"><span data-stu-id="67ff3-123">-Context</span></span>
<span data-ttu-id="67ff3-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="67ff3-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="67ff3-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-125">This parameter is required.</span></span>

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

### <span data-ttu-id="67ff3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ff3-126">-DefaultProfile</span></span>
<span data-ttu-id="67ff3-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67ff3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ff3-128">-描述</span><span class="sxs-lookup"><span data-stu-id="67ff3-128">-Description</span></span>
<span data-ttu-id="67ff3-129">快取說明。</span><span class="sxs-lookup"><span data-stu-id="67ff3-129">Cache Description.</span></span>
<span data-ttu-id="67ff3-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="67ff3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ff3-131">-InputObject</span></span>
<span data-ttu-id="67ff3-132">PsApiManagementCache 的實例。</span><span class="sxs-lookup"><span data-stu-id="67ff3-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="67ff3-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-133">This parameter is required.</span></span>

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

### <span data-ttu-id="67ff3-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67ff3-134">-PassThru</span></span>
<span data-ttu-id="67ff3-135">如果已指定，則 ServiceManagement 的 ApiManagement 實例，代表修改過的快取的 PsApiManagementCache 類型將會寫入輸出中。</span><span class="sxs-lookup"><span data-stu-id="67ff3-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="67ff3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ff3-136">-ResourceId</span></span>
<span data-ttu-id="67ff3-137">[快取] 的 [Arm] ResourceId。</span><span class="sxs-lookup"><span data-stu-id="67ff3-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="67ff3-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="67ff3-138">This parameter is required.</span></span>

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

### <span data-ttu-id="67ff3-139">-確認</span><span class="sxs-lookup"><span data-stu-id="67ff3-139">-Confirm</span></span>
<span data-ttu-id="67ff3-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67ff3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ff3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ff3-141">-WhatIf</span></span>
<span data-ttu-id="67ff3-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67ff3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ff3-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67ff3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ff3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ff3-144">CommonParameters</span></span>
<span data-ttu-id="67ff3-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67ff3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ff3-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67ff3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ff3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="67ff3-147">INPUTS</span></span>

### <span data-ttu-id="67ff3-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="67ff3-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="67ff3-149">System.object</span><span class="sxs-lookup"><span data-stu-id="67ff3-149">System.String</span></span>

### <span data-ttu-id="67ff3-150">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="67ff3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="67ff3-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="67ff3-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67ff3-152">輸出</span><span class="sxs-lookup"><span data-stu-id="67ff3-152">OUTPUTS</span></span>

### <span data-ttu-id="67ff3-153">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="67ff3-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="67ff3-154">筆記</span><span class="sxs-lookup"><span data-stu-id="67ff3-154">NOTES</span></span>

## <span data-ttu-id="67ff3-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="67ff3-155">RELATED LINKS</span></span>

[<span data-ttu-id="67ff3-156">新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67ff3-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="67ff3-157">AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67ff3-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="67ff3-158">移除-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67ff3-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)