---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: a95be9f18c00d72afb6117d1689f62a6bad053b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398677"
---
# <span data-ttu-id="4ecf9-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4ecf9-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="4ecf9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ecf9-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecf9-103">移除緩存實體。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-103">Removes the cache entity.</span></span>

## <span data-ttu-id="4ecf9-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ecf9-104">SYNTAX</span></span>

### <span data-ttu-id="4ecf9-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="4ecf9-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ecf9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ecf9-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ecf9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ecf9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ecf9-108">描述</span><span class="sxs-lookup"><span data-stu-id="4ecf9-108">DESCRIPTION</span></span>
<span data-ttu-id="4ecf9-109">Cmdlet **Remove-AzApiManagementCache 會** 移除緩存實體。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="4ecf9-110">例子</span><span class="sxs-lookup"><span data-stu-id="4ecf9-110">EXAMPLES</span></span>

### <span data-ttu-id="4ecf9-111">範例 1：移除 Cache 實體</span><span class="sxs-lookup"><span data-stu-id="4ecf9-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="4ecf9-112">此 Cmdlet 會從 `centralus` Api 管理服務移除緩存。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="4ecf9-113">參數</span><span class="sxs-lookup"><span data-stu-id="4ecf9-113">PARAMETERS</span></span>

### <span data-ttu-id="4ecf9-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4ecf9-114">-CacheId</span></span>
<span data-ttu-id="4ecf9-115">現有 cacheId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="4ecf9-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-116">This parameter is required.</span></span>

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

### <span data-ttu-id="4ecf9-117">-內容</span><span class="sxs-lookup"><span data-stu-id="4ecf9-117">-Context</span></span>
<span data-ttu-id="4ecf9-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4ecf9-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-119">This parameter is required.</span></span>

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

### <span data-ttu-id="4ecf9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecf9-120">-DefaultProfile</span></span>
<span data-ttu-id="4ecf9-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecf9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ecf9-122">-InputObject</span></span>
<span data-ttu-id="4ecf9-123">PsApiManagementCache 實例。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="4ecf9-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="4ecf9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ecf9-125">-PassThru</span></span>
<span data-ttu-id="4ecf9-126">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4ecf9-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-127">This parameter is optional.</span></span>
<span data-ttu-id="4ecf9-128">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-128">Default value is false.</span></span>

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

### <span data-ttu-id="4ecf9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ecf9-129">-ResourceId</span></span>
<span data-ttu-id="4ecf9-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="4ecf9-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="4ecf9-131">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-131">This parameter is required.</span></span>

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

### <span data-ttu-id="4ecf9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4ecf9-132">-Confirm</span></span>
<span data-ttu-id="4ecf9-133">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecf9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecf9-134">-WhatIf</span></span>
<span data-ttu-id="4ecf9-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ecf9-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecf9-137">CommonParameters</span></span>
<span data-ttu-id="4ecf9-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ecf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecf9-139">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ecf9-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecf9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4ecf9-140">INPUTS</span></span>

### <span data-ttu-id="4ecf9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4ecf9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ecf9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4ecf9-142">System.String</span></span>

### <span data-ttu-id="4ecf9-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ecf9-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ecf9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4ecf9-144">OUTPUTS</span></span>

### <span data-ttu-id="4ecf9-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ecf9-145">System.Boolean</span></span>

## <span data-ttu-id="4ecf9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4ecf9-146">NOTES</span></span>

## <span data-ttu-id="4ecf9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ecf9-147">RELATED LINKS</span></span>

[<span data-ttu-id="4ecf9-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4ecf9-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="4ecf9-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4ecf9-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="4ecf9-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4ecf9-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
