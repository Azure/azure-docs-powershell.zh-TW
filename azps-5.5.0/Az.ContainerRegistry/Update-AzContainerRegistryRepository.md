---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137458"
---
# <span data-ttu-id="95d35-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="95d35-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="95d35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95d35-102">SYNOPSIS</span></span>
<span data-ttu-id="95d35-103">更新 ACR 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="95d35-103">Update ACR repository.</span></span>

## <span data-ttu-id="95d35-104">句法</span><span class="sxs-lookup"><span data-stu-id="95d35-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d35-105">說明</span><span class="sxs-lookup"><span data-stu-id="95d35-105">DESCRIPTION</span></span>
<span data-ttu-id="95d35-106">更新 ACR 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="95d35-106">Update ACR repository.</span></span>

## <span data-ttu-id="95d35-107">示例</span><span class="sxs-lookup"><span data-stu-id="95d35-107">EXAMPLES</span></span>

### <span data-ttu-id="95d35-108">範例1</span><span class="sxs-lookup"><span data-stu-id="95d35-108">Example 1</span></span>
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

<span data-ttu-id="95d35-109">在 [registry] 下更新 [知識庫] 高山屬性。</span><span class="sxs-lookup"><span data-stu-id="95d35-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="95d35-110">參數</span><span class="sxs-lookup"><span data-stu-id="95d35-110">PARAMETERS</span></span>

### <span data-ttu-id="95d35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d35-111">-DefaultProfile</span></span>
<span data-ttu-id="95d35-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95d35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d35-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="95d35-113">-DeleteEnabled</span></span>
<span data-ttu-id="95d35-114">刪除 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="95d35-114">Delete enable.</span></span>

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

### <span data-ttu-id="95d35-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="95d35-115">-ListEnabled</span></span>
<span data-ttu-id="95d35-116">清單啟用]。</span><span class="sxs-lookup"><span data-stu-id="95d35-116">List enable.</span></span>

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

### <span data-ttu-id="95d35-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="95d35-117">-Name</span></span>
<span data-ttu-id="95d35-118">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="95d35-118">Repository Name.</span></span>

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

### <span data-ttu-id="95d35-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="95d35-119">-ReadEnabled</span></span>
<span data-ttu-id="95d35-120">已閱讀 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="95d35-120">Read enable.</span></span>

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

### <span data-ttu-id="95d35-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="95d35-121">-RegistryName</span></span>
<span data-ttu-id="95d35-122">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="95d35-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="95d35-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="95d35-123">-WriteEnabled</span></span>
<span data-ttu-id="95d35-124">啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="95d35-124">Write enable.</span></span>

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

### <span data-ttu-id="95d35-125">-確認</span><span class="sxs-lookup"><span data-stu-id="95d35-125">-Confirm</span></span>
<span data-ttu-id="95d35-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95d35-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d35-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d35-127">-WhatIf</span></span>
<span data-ttu-id="95d35-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95d35-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d35-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95d35-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d35-130">CommonParameters</span></span>
<span data-ttu-id="95d35-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95d35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d35-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95d35-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d35-133">輸入</span><span class="sxs-lookup"><span data-stu-id="95d35-133">INPUTS</span></span>

### <span data-ttu-id="95d35-134">System.object</span><span class="sxs-lookup"><span data-stu-id="95d35-134">System.String</span></span>

## <span data-ttu-id="95d35-135">輸出</span><span class="sxs-lookup"><span data-stu-id="95d35-135">OUTPUTS</span></span>

### <span data-ttu-id="95d35-136">PSRepositoryAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="95d35-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="95d35-137">筆記</span><span class="sxs-lookup"><span data-stu-id="95d35-137">NOTES</span></span>

## <span data-ttu-id="95d35-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="95d35-138">RELATED LINKS</span></span>
