---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447464"
---
# <span data-ttu-id="a70b9-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a70b9-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="a70b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a70b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a70b9-103">建立新的快取實體</span><span class="sxs-lookup"><span data-stu-id="a70b9-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="a70b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a70b9-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="a70b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a70b9-106">Cmdlet [ **new-AzApiManagementCache** ] 會在 Api 管理服務中建立新的快取實體。</span><span class="sxs-lookup"><span data-stu-id="a70b9-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="a70b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="a70b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a70b9-108">範例1：建立新的快取實體</span><span class="sxs-lookup"><span data-stu-id="a70b9-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="a70b9-109">Cmdlet 會在 Api 管理服務的主位置中建立新的快取實體。</span><span class="sxs-lookup"><span data-stu-id="a70b9-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="a70b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="a70b9-110">PARAMETERS</span></span>

### <span data-ttu-id="a70b9-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="a70b9-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="a70b9-112">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a70b9-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="a70b9-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a70b9-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="a70b9-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a70b9-114">-CacheId</span></span>
<span data-ttu-id="a70b9-115">新快取的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a70b9-115">Identifier of new cache.</span></span>
<span data-ttu-id="a70b9-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a70b9-116">This parameter is optional.</span></span>
<span data-ttu-id="a70b9-117">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="a70b9-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="a70b9-118">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a70b9-118">-ConnectionString</span></span>
<span data-ttu-id="a70b9-119">Redis [連接字串]。</span><span class="sxs-lookup"><span data-stu-id="a70b9-119">Redis Connection String.</span></span>
<span data-ttu-id="a70b9-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a70b9-120">This parameter is required.</span></span>

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

### <span data-ttu-id="a70b9-121">-內容</span><span class="sxs-lookup"><span data-stu-id="a70b9-121">-Context</span></span>
<span data-ttu-id="a70b9-122">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a70b9-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a70b9-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a70b9-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a70b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70b9-124">-DefaultProfile</span></span>
<span data-ttu-id="a70b9-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a70b9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a70b9-126">-描述</span><span class="sxs-lookup"><span data-stu-id="a70b9-126">-Description</span></span>
<span data-ttu-id="a70b9-127">快取說明。</span><span class="sxs-lookup"><span data-stu-id="a70b9-127">Cache Description.</span></span>
<span data-ttu-id="a70b9-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a70b9-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="a70b9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a70b9-129">-Confirm</span></span>
<span data-ttu-id="a70b9-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a70b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70b9-131">-WhatIf</span></span>
<span data-ttu-id="a70b9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a70b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70b9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a70b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70b9-134">CommonParameters</span></span>
<span data-ttu-id="a70b9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a70b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70b9-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a70b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70b9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a70b9-137">INPUTS</span></span>

### <span data-ttu-id="a70b9-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a70b9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a70b9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a70b9-139">System.String</span></span>

## <span data-ttu-id="a70b9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a70b9-140">OUTPUTS</span></span>

### <span data-ttu-id="a70b9-141">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a70b9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="a70b9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a70b9-142">NOTES</span></span>

## <span data-ttu-id="a70b9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a70b9-143">RELATED LINKS</span></span>

[<span data-ttu-id="a70b9-144">AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a70b9-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="a70b9-145">移除-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a70b9-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="a70b9-146">更新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a70b9-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
