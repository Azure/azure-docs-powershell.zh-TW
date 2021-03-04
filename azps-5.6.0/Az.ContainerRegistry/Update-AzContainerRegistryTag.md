---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902990"
---
# <span data-ttu-id="fc26c-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="fc26c-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="fc26c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc26c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc26c-103">更新 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="fc26c-103">Update ACR tag.</span></span>

## <span data-ttu-id="fc26c-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc26c-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc26c-105">描述</span><span class="sxs-lookup"><span data-stu-id="fc26c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc26c-106">更新 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="fc26c-106">Update ACR tag.</span></span>
<span data-ttu-id="fc26c-107">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="fc26c-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="fc26c-108">第一。</span><span class="sxs-lookup"><span data-stu-id="fc26c-108">first.</span></span>

## <span data-ttu-id="fc26c-109">例子</span><span class="sxs-lookup"><span data-stu-id="fc26c-109">EXAMPLES</span></span>

### <span data-ttu-id="fc26c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="fc26c-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="fc26c-111">在註冊表下更新最新標記的屬性。</span><span class="sxs-lookup"><span data-stu-id="fc26c-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="fc26c-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc26c-112">PARAMETERS</span></span>

### <span data-ttu-id="fc26c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc26c-113">-DefaultProfile</span></span>
<span data-ttu-id="fc26c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc26c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc26c-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="fc26c-115">-DeleteEnabled</span></span>
<span data-ttu-id="fc26c-116">刪除啟用。</span><span class="sxs-lookup"><span data-stu-id="fc26c-116">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc26c-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="fc26c-117">-ListEnabled</span></span>
<span data-ttu-id="fc26c-118">清單啟用。</span><span class="sxs-lookup"><span data-stu-id="fc26c-118">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc26c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc26c-119">-Name</span></span>
<span data-ttu-id="fc26c-120">標記。</span><span class="sxs-lookup"><span data-stu-id="fc26c-120">Tag.</span></span>

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

### <span data-ttu-id="fc26c-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="fc26c-121">-ReadEnabled</span></span>
<span data-ttu-id="fc26c-122">讀取啟用。</span><span class="sxs-lookup"><span data-stu-id="fc26c-122">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc26c-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fc26c-123">-RegistryName</span></span>
<span data-ttu-id="fc26c-124">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="fc26c-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="fc26c-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="fc26c-125">-RepositoryName</span></span>
<span data-ttu-id="fc26c-126">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fc26c-126">Repository Name.</span></span>

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

### <span data-ttu-id="fc26c-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="fc26c-127">-WriteEnabled</span></span>
<span data-ttu-id="fc26c-128">寫入啟用。</span><span class="sxs-lookup"><span data-stu-id="fc26c-128">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc26c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fc26c-129">-Confirm</span></span>
<span data-ttu-id="fc26c-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fc26c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc26c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc26c-131">-WhatIf</span></span>
<span data-ttu-id="fc26c-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc26c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc26c-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc26c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc26c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc26c-134">CommonParameters</span></span>
<span data-ttu-id="fc26c-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc26c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc26c-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc26c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc26c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fc26c-137">INPUTS</span></span>

### <span data-ttu-id="fc26c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fc26c-138">System.String</span></span>

## <span data-ttu-id="fc26c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fc26c-139">OUTPUTS</span></span>

### <span data-ttu-id="fc26c-140">Microsoft.Azure.Commands.ContainerRegistry.models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="fc26c-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="fc26c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fc26c-141">NOTES</span></span>

## <span data-ttu-id="fc26c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc26c-142">RELATED LINKS</span></span>
