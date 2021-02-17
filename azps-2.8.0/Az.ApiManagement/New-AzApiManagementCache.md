---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: d4095c1a20c4cebc3fb5f9b58f6f696c9cf41dc7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399408"
---
# <span data-ttu-id="59539-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59539-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="59539-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59539-102">SYNOPSIS</span></span>
<span data-ttu-id="59539-103">建立新的 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="59539-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="59539-104">語法</span><span class="sxs-lookup"><span data-stu-id="59539-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59539-105">描述</span><span class="sxs-lookup"><span data-stu-id="59539-105">DESCRIPTION</span></span>
<span data-ttu-id="59539-106">Cmdlet **New-AzApiManagementCache** 在 Api 管理服務中建立新緩存實體。</span><span class="sxs-lookup"><span data-stu-id="59539-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="59539-107">例子</span><span class="sxs-lookup"><span data-stu-id="59539-107">EXAMPLES</span></span>

### <span data-ttu-id="59539-108">範例 1：建立新 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="59539-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="59539-109">Cmdlet 會于 Api 管理服務的主位置中建立新緩存實體。</span><span class="sxs-lookup"><span data-stu-id="59539-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="59539-110">參數</span><span class="sxs-lookup"><span data-stu-id="59539-110">PARAMETERS</span></span>

### <span data-ttu-id="59539-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="59539-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="59539-112">Azure Redis Cache 實例的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="59539-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="59539-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="59539-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="59539-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="59539-114">-CacheId</span></span>
<span data-ttu-id="59539-115">新緩存的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59539-115">Identifier of new cache.</span></span>
<span data-ttu-id="59539-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="59539-116">This parameter is optional.</span></span>
<span data-ttu-id="59539-117">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="59539-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="59539-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="59539-118">-ConnectionString</span></span>
<span data-ttu-id="59539-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="59539-119">Redis Connection String.</span></span>
<span data-ttu-id="59539-120">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="59539-120">This parameter is required.</span></span>

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

### <span data-ttu-id="59539-121">-內容</span><span class="sxs-lookup"><span data-stu-id="59539-121">-Context</span></span>
<span data-ttu-id="59539-122">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="59539-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="59539-123">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="59539-123">This parameter is required.</span></span>

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

### <span data-ttu-id="59539-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59539-124">-DefaultProfile</span></span>
<span data-ttu-id="59539-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="59539-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59539-126">-描述</span><span class="sxs-lookup"><span data-stu-id="59539-126">-Description</span></span>
<span data-ttu-id="59539-127">緩存描述。</span><span class="sxs-lookup"><span data-stu-id="59539-127">Cache Description.</span></span>
<span data-ttu-id="59539-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="59539-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="59539-129">-確認</span><span class="sxs-lookup"><span data-stu-id="59539-129">-Confirm</span></span>
<span data-ttu-id="59539-130">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="59539-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59539-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59539-131">-WhatIf</span></span>
<span data-ttu-id="59539-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59539-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59539-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59539-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59539-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59539-134">CommonParameters</span></span>
<span data-ttu-id="59539-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59539-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59539-136">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59539-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59539-137">輸入</span><span class="sxs-lookup"><span data-stu-id="59539-137">INPUTS</span></span>

### <span data-ttu-id="59539-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="59539-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59539-139">System.String</span><span class="sxs-lookup"><span data-stu-id="59539-139">System.String</span></span>

## <span data-ttu-id="59539-140">輸出</span><span class="sxs-lookup"><span data-stu-id="59539-140">OUTPUTS</span></span>

### <span data-ttu-id="59539-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59539-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="59539-142">筆記</span><span class="sxs-lookup"><span data-stu-id="59539-142">NOTES</span></span>

## <span data-ttu-id="59539-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="59539-143">RELATED LINKS</span></span>

[<span data-ttu-id="59539-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59539-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="59539-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59539-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="59539-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59539-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
