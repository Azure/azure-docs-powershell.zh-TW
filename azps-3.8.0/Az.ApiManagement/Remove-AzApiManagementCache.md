---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: b43aba64f30c4a1987f2bcd8dec3edb7834f2082
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958170"
---
# <span data-ttu-id="a4258-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a4258-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="a4258-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4258-102">SYNOPSIS</span></span>
<span data-ttu-id="a4258-103">移除快取實體。</span><span class="sxs-lookup"><span data-stu-id="a4258-103">Removes the cache entity.</span></span>

## <span data-ttu-id="a4258-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4258-104">SYNTAX</span></span>

### <span data-ttu-id="a4258-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="a4258-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4258-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4258-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4258-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4258-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4258-108">說明</span><span class="sxs-lookup"><span data-stu-id="a4258-108">DESCRIPTION</span></span>
<span data-ttu-id="a4258-109">Cmdlet **移除-AzApiManagementCache** 會移除快取實體。</span><span class="sxs-lookup"><span data-stu-id="a4258-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="a4258-110">示例</span><span class="sxs-lookup"><span data-stu-id="a4258-110">EXAMPLES</span></span>

### <span data-ttu-id="a4258-111">範例1：移除快取實體</span><span class="sxs-lookup"><span data-stu-id="a4258-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="a4258-112">這個 Cmdlet 會 `centralus` 從 Api 管理服務移除快取。</span><span class="sxs-lookup"><span data-stu-id="a4258-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="a4258-113">參數</span><span class="sxs-lookup"><span data-stu-id="a4258-113">PARAMETERS</span></span>

### <span data-ttu-id="a4258-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a4258-114">-CacheId</span></span>
<span data-ttu-id="a4258-115">現有 cacheId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4258-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="a4258-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4258-116">This parameter is required.</span></span>

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

### <span data-ttu-id="a4258-117">-內容</span><span class="sxs-lookup"><span data-stu-id="a4258-117">-Context</span></span>
<span data-ttu-id="a4258-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a4258-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a4258-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4258-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a4258-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4258-120">-DefaultProfile</span></span>
<span data-ttu-id="a4258-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4258-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4258-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4258-122">-InputObject</span></span>
<span data-ttu-id="a4258-123">PsApiManagementCache 的實例。</span><span class="sxs-lookup"><span data-stu-id="a4258-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="a4258-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4258-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a4258-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4258-125">-PassThru</span></span>
<span data-ttu-id="a4258-126">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="a4258-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a4258-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a4258-127">This parameter is optional.</span></span>
<span data-ttu-id="a4258-128">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="a4258-128">Default value is false.</span></span>

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

### <span data-ttu-id="a4258-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4258-129">-ResourceId</span></span>
<span data-ttu-id="a4258-130">[快取] 的 [Arm] ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a4258-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="a4258-131">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4258-131">This parameter is required.</span></span>

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

### <span data-ttu-id="a4258-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a4258-132">-Confirm</span></span>
<span data-ttu-id="a4258-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4258-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4258-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4258-134">-WhatIf</span></span>
<span data-ttu-id="a4258-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4258-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4258-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4258-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4258-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4258-137">CommonParameters</span></span>
<span data-ttu-id="a4258-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4258-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4258-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4258-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4258-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a4258-140">INPUTS</span></span>

### <span data-ttu-id="a4258-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a4258-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4258-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a4258-142">System.String</span></span>

### <span data-ttu-id="a4258-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a4258-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a4258-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a4258-144">OUTPUTS</span></span>

### <span data-ttu-id="a4258-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a4258-145">System.Boolean</span></span>

## <span data-ttu-id="a4258-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a4258-146">NOTES</span></span>

## <span data-ttu-id="a4258-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4258-147">RELATED LINKS</span></span>

[<span data-ttu-id="a4258-148">新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a4258-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="a4258-149">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a4258-149">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="a4258-150">AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a4258-150">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)