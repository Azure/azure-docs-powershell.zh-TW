---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398099"
---
# <span data-ttu-id="b9455-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b9455-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="b9455-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9455-102">SYNOPSIS</span></span>
<span data-ttu-id="b9455-103">建立新的 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="b9455-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="b9455-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9455-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9455-105">描述</span><span class="sxs-lookup"><span data-stu-id="b9455-105">DESCRIPTION</span></span>
<span data-ttu-id="b9455-106">Cmdlet **New-AzApiManagementCache** 在 Api 管理服務中建立新緩存實體。</span><span class="sxs-lookup"><span data-stu-id="b9455-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="b9455-107">例子</span><span class="sxs-lookup"><span data-stu-id="b9455-107">EXAMPLES</span></span>

### <span data-ttu-id="b9455-108">範例 1：建立新 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="b9455-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="b9455-109">Cmdlet 會于 Api 管理服務的主位置中建立新緩存實體。</span><span class="sxs-lookup"><span data-stu-id="b9455-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="b9455-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9455-110">PARAMETERS</span></span>

### <span data-ttu-id="b9455-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="b9455-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="b9455-112">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b9455-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="b9455-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b9455-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="b9455-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b9455-114">-CacheId</span></span>
<span data-ttu-id="b9455-115">新緩存的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9455-115">Identifier of new cache.</span></span>
<span data-ttu-id="b9455-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b9455-116">This parameter is optional.</span></span>
<span data-ttu-id="b9455-117">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="b9455-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b9455-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b9455-118">-ConnectionString</span></span>
<span data-ttu-id="b9455-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="b9455-119">Redis Connection String.</span></span>
<span data-ttu-id="b9455-120">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="b9455-120">This parameter is required.</span></span>

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

### <span data-ttu-id="b9455-121">-內容</span><span class="sxs-lookup"><span data-stu-id="b9455-121">-Context</span></span>
<span data-ttu-id="b9455-122">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b9455-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b9455-123">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="b9455-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b9455-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9455-124">-DefaultProfile</span></span>
<span data-ttu-id="b9455-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9455-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9455-126">-描述</span><span class="sxs-lookup"><span data-stu-id="b9455-126">-Description</span></span>
<span data-ttu-id="b9455-127">緩存描述。</span><span class="sxs-lookup"><span data-stu-id="b9455-127">Cache Description.</span></span>
<span data-ttu-id="b9455-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b9455-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="b9455-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b9455-129">-Confirm</span></span>
<span data-ttu-id="b9455-130">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b9455-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9455-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9455-131">-WhatIf</span></span>
<span data-ttu-id="b9455-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9455-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9455-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9455-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9455-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9455-134">CommonParameters</span></span>
<span data-ttu-id="b9455-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9455-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9455-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9455-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9455-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b9455-137">INPUTS</span></span>

### <span data-ttu-id="b9455-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b9455-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9455-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b9455-139">System.String</span></span>

## <span data-ttu-id="b9455-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b9455-140">OUTPUTS</span></span>

### <span data-ttu-id="b9455-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b9455-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="b9455-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b9455-142">NOTES</span></span>

## <span data-ttu-id="b9455-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9455-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9455-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b9455-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b9455-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b9455-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="b9455-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b9455-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
