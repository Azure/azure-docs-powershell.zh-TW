---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: 0e0fa81830264f550531a156260f3a4f2c7827ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613933"
---
# <span data-ttu-id="39fd5-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="39fd5-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="39fd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="39fd5-103">移除快取實體。</span><span class="sxs-lookup"><span data-stu-id="39fd5-103">Removes the cache entity.</span></span>

## <span data-ttu-id="39fd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="39fd5-104">SYNTAX</span></span>

### <span data-ttu-id="39fd5-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="39fd5-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fd5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fd5-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39fd5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39fd5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39fd5-108">說明</span><span class="sxs-lookup"><span data-stu-id="39fd5-108">DESCRIPTION</span></span>
<span data-ttu-id="39fd5-109">Cmdlet **移除-AzApiManagementCache** 會移除快取實體。</span><span class="sxs-lookup"><span data-stu-id="39fd5-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="39fd5-110">示例</span><span class="sxs-lookup"><span data-stu-id="39fd5-110">EXAMPLES</span></span>

### <span data-ttu-id="39fd5-111">範例1：移除快取實體</span><span class="sxs-lookup"><span data-stu-id="39fd5-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="39fd5-112">這個 Cmdlet 會 `centralus` 從 Api 管理服務移除快取。</span><span class="sxs-lookup"><span data-stu-id="39fd5-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="39fd5-113">參數</span><span class="sxs-lookup"><span data-stu-id="39fd5-113">PARAMETERS</span></span>

### <span data-ttu-id="39fd5-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="39fd5-114">-CacheId</span></span>
<span data-ttu-id="39fd5-115">現有 cacheId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fd5-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="39fd5-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39fd5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="39fd5-117">-內容</span><span class="sxs-lookup"><span data-stu-id="39fd5-117">-Context</span></span>
<span data-ttu-id="39fd5-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="39fd5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="39fd5-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39fd5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="39fd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39fd5-120">-DefaultProfile</span></span>
<span data-ttu-id="39fd5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39fd5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39fd5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39fd5-122">-InputObject</span></span>
<span data-ttu-id="39fd5-123">PsApiManagementCache 的實例。</span><span class="sxs-lookup"><span data-stu-id="39fd5-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="39fd5-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39fd5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="39fd5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39fd5-125">-PassThru</span></span>
<span data-ttu-id="39fd5-126">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="39fd5-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="39fd5-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="39fd5-127">This parameter is optional.</span></span>
<span data-ttu-id="39fd5-128">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="39fd5-128">Default value is false.</span></span>

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

### <span data-ttu-id="39fd5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39fd5-129">-ResourceId</span></span>
<span data-ttu-id="39fd5-130">[快取] 的 [Arm] ResourceId。</span><span class="sxs-lookup"><span data-stu-id="39fd5-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="39fd5-131">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39fd5-131">This parameter is required.</span></span>

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

### <span data-ttu-id="39fd5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="39fd5-132">-Confirm</span></span>
<span data-ttu-id="39fd5-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39fd5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39fd5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39fd5-134">-WhatIf</span></span>
<span data-ttu-id="39fd5-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39fd5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39fd5-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39fd5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39fd5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39fd5-137">CommonParameters</span></span>
<span data-ttu-id="39fd5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39fd5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39fd5-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39fd5-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39fd5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="39fd5-140">INPUTS</span></span>

### <span data-ttu-id="39fd5-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="39fd5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39fd5-142">System.object</span><span class="sxs-lookup"><span data-stu-id="39fd5-142">System.String</span></span>

### <span data-ttu-id="39fd5-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="39fd5-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39fd5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="39fd5-144">OUTPUTS</span></span>

### <span data-ttu-id="39fd5-145">System.object</span><span class="sxs-lookup"><span data-stu-id="39fd5-145">System.Boolean</span></span>

## <span data-ttu-id="39fd5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="39fd5-146">NOTES</span></span>

## <span data-ttu-id="39fd5-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="39fd5-147">RELATED LINKS</span></span>

[<span data-ttu-id="39fd5-148">新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="39fd5-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="39fd5-149">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="39fd5-149">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="39fd5-150">AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="39fd5-150">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)