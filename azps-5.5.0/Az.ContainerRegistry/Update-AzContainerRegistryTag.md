---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141182"
---
# <span data-ttu-id="43ead-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="43ead-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="43ead-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43ead-102">SYNOPSIS</span></span>
<span data-ttu-id="43ead-103">更新 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="43ead-103">Update ACR tag.</span></span>

## <span data-ttu-id="43ead-104">句法</span><span class="sxs-lookup"><span data-stu-id="43ead-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ead-105">說明</span><span class="sxs-lookup"><span data-stu-id="43ead-105">DESCRIPTION</span></span>
<span data-ttu-id="43ead-106">更新 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="43ead-106">Update ACR tag.</span></span>
<span data-ttu-id="43ead-107">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="43ead-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="43ead-108">一.</span><span class="sxs-lookup"><span data-stu-id="43ead-108">first.</span></span>

## <span data-ttu-id="43ead-109">示例</span><span class="sxs-lookup"><span data-stu-id="43ead-109">EXAMPLES</span></span>

### <span data-ttu-id="43ead-110">範例1</span><span class="sxs-lookup"><span data-stu-id="43ead-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="43ead-111">更新 [registry] 下的 [標記最新] 屬性。</span><span class="sxs-lookup"><span data-stu-id="43ead-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="43ead-112">參數</span><span class="sxs-lookup"><span data-stu-id="43ead-112">PARAMETERS</span></span>

### <span data-ttu-id="43ead-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ead-113">-DefaultProfile</span></span>
<span data-ttu-id="43ead-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43ead-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ead-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="43ead-115">-DeleteEnabled</span></span>
<span data-ttu-id="43ead-116">刪除 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="43ead-116">Delete enable.</span></span>

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

### <span data-ttu-id="43ead-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="43ead-117">-ListEnabled</span></span>
<span data-ttu-id="43ead-118">清單啟用]。</span><span class="sxs-lookup"><span data-stu-id="43ead-118">List enable.</span></span>

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

### <span data-ttu-id="43ead-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="43ead-119">-Name</span></span>
<span data-ttu-id="43ead-120">標記.</span><span class="sxs-lookup"><span data-stu-id="43ead-120">Tag.</span></span>

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

### <span data-ttu-id="43ead-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="43ead-121">-ReadEnabled</span></span>
<span data-ttu-id="43ead-122">已閱讀 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="43ead-122">Read enable.</span></span>

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

### <span data-ttu-id="43ead-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="43ead-123">-RegistryName</span></span>
<span data-ttu-id="43ead-124">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="43ead-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="43ead-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="43ead-125">-RepositoryName</span></span>
<span data-ttu-id="43ead-126">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="43ead-126">Repository Name.</span></span>

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

### <span data-ttu-id="43ead-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="43ead-127">-WriteEnabled</span></span>
<span data-ttu-id="43ead-128">啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="43ead-128">Write enable.</span></span>

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

### <span data-ttu-id="43ead-129">-確認</span><span class="sxs-lookup"><span data-stu-id="43ead-129">-Confirm</span></span>
<span data-ttu-id="43ead-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43ead-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ead-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ead-131">-WhatIf</span></span>
<span data-ttu-id="43ead-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43ead-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ead-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43ead-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ead-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ead-134">CommonParameters</span></span>
<span data-ttu-id="43ead-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43ead-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ead-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43ead-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ead-137">輸入</span><span class="sxs-lookup"><span data-stu-id="43ead-137">INPUTS</span></span>

### <span data-ttu-id="43ead-138">System.object</span><span class="sxs-lookup"><span data-stu-id="43ead-138">System.String</span></span>

## <span data-ttu-id="43ead-139">輸出</span><span class="sxs-lookup"><span data-stu-id="43ead-139">OUTPUTS</span></span>

### <span data-ttu-id="43ead-140">PSTagAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="43ead-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="43ead-141">筆記</span><span class="sxs-lookup"><span data-stu-id="43ead-141">NOTES</span></span>

## <span data-ttu-id="43ead-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="43ead-142">RELATED LINKS</span></span>
