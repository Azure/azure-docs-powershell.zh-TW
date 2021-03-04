---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: 45572cbd2255a604e492c7740d1749a0ad968845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902993"
---
# <span data-ttu-id="dc577-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="dc577-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="dc577-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc577-102">SYNOPSIS</span></span>
<span data-ttu-id="dc577-103">更新 ACR 存放庫。</span><span class="sxs-lookup"><span data-stu-id="dc577-103">Update ACR repository.</span></span>

## <span data-ttu-id="dc577-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc577-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc577-105">描述</span><span class="sxs-lookup"><span data-stu-id="dc577-105">DESCRIPTION</span></span>
<span data-ttu-id="dc577-106">更新 ACR 存放庫。</span><span class="sxs-lookup"><span data-stu-id="dc577-106">Update ACR repository.</span></span>

## <span data-ttu-id="dc577-107">例子</span><span class="sxs-lookup"><span data-stu-id="dc577-107">EXAMPLES</span></span>

### <span data-ttu-id="dc577-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="dc577-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="dc577-109">在註冊表下更新存放庫高山的屬性。</span><span class="sxs-lookup"><span data-stu-id="dc577-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="dc577-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc577-110">PARAMETERS</span></span>

### <span data-ttu-id="dc577-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc577-111">-DefaultProfile</span></span>
<span data-ttu-id="dc577-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc577-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc577-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="dc577-113">-DeleteEnabled</span></span>
<span data-ttu-id="dc577-114">刪除啟用。</span><span class="sxs-lookup"><span data-stu-id="dc577-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc577-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="dc577-115">-ListEnabled</span></span>
<span data-ttu-id="dc577-116">清單啟用。</span><span class="sxs-lookup"><span data-stu-id="dc577-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc577-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc577-117">-Name</span></span>
<span data-ttu-id="dc577-118">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="dc577-118">Repository Name.</span></span>

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

### <span data-ttu-id="dc577-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="dc577-119">-ReadEnabled</span></span>
<span data-ttu-id="dc577-120">讀取啟用。</span><span class="sxs-lookup"><span data-stu-id="dc577-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc577-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="dc577-121">-RegistryName</span></span>
<span data-ttu-id="dc577-122">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="dc577-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="dc577-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="dc577-123">-WriteEnabled</span></span>
<span data-ttu-id="dc577-124">寫入啟用。</span><span class="sxs-lookup"><span data-stu-id="dc577-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc577-125">-確認</span><span class="sxs-lookup"><span data-stu-id="dc577-125">-Confirm</span></span>
<span data-ttu-id="dc577-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dc577-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc577-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc577-127">-WhatIf</span></span>
<span data-ttu-id="dc577-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc577-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc577-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc577-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc577-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc577-130">CommonParameters</span></span>
<span data-ttu-id="dc577-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc577-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc577-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc577-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc577-133">輸入</span><span class="sxs-lookup"><span data-stu-id="dc577-133">INPUTS</span></span>

### <span data-ttu-id="dc577-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dc577-134">System.String</span></span>

## <span data-ttu-id="dc577-135">輸出</span><span class="sxs-lookup"><span data-stu-id="dc577-135">OUTPUTS</span></span>

### <span data-ttu-id="dc577-136">Microsoft.Azure.Commands.ContainerRegistry.models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="dc577-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="dc577-137">筆記</span><span class="sxs-lookup"><span data-stu-id="dc577-137">NOTES</span></span>

## <span data-ttu-id="dc577-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc577-138">RELATED LINKS</span></span>
