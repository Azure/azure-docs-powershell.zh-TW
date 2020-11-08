---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136003"
---
# <span data-ttu-id="a425b-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a425b-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="a425b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a425b-102">SYNOPSIS</span></span>
<span data-ttu-id="a425b-103">更新專案來源。</span><span class="sxs-lookup"><span data-stu-id="a425b-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="a425b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a425b-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a425b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a425b-105">DESCRIPTION</span></span>
<span data-ttu-id="a425b-106">**AzDeploymentManagerArtifactSource** Cmdlet 會使用指定的專案源物件更新專案來源。</span><span class="sxs-lookup"><span data-stu-id="a425b-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="a425b-107">這個 Cmdlet 會傳回更新的 ArtifactSource 物件。</span><span class="sxs-lookup"><span data-stu-id="a425b-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="a425b-108">示例</span><span class="sxs-lookup"><span data-stu-id="a425b-108">EXAMPLES</span></span>

### <span data-ttu-id="a425b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a425b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="a425b-110">這個命令會分別更新名稱和 ResourceGroup 與 $artifactSourceObject 的 Name 及 ResourceGroupName 屬性相符的專案來源。</span><span class="sxs-lookup"><span data-stu-id="a425b-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="a425b-111">專案來源會更新為 $artifactSourceObject 中設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="a425b-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="a425b-112">參數</span><span class="sxs-lookup"><span data-stu-id="a425b-112">PARAMETERS</span></span>

### <span data-ttu-id="a425b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a425b-113">-DefaultProfile</span></span>
<span data-ttu-id="a425b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a425b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a425b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a425b-115">-InputObject</span></span>
<span data-ttu-id="a425b-116">專案來源物件。</span><span class="sxs-lookup"><span data-stu-id="a425b-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a425b-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a425b-117">-Confirm</span></span>
<span data-ttu-id="a425b-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a425b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a425b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a425b-119">-WhatIf</span></span>
<span data-ttu-id="a425b-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a425b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a425b-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a425b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a425b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a425b-122">CommonParameters</span></span>
<span data-ttu-id="a425b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a425b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a425b-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a425b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a425b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a425b-125">INPUTS</span></span>

### <span data-ttu-id="a425b-126">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="a425b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a425b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a425b-127">OUTPUTS</span></span>

### <span data-ttu-id="a425b-128">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="a425b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a425b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a425b-129">NOTES</span></span>

## <span data-ttu-id="a425b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a425b-130">RELATED LINKS</span></span>
