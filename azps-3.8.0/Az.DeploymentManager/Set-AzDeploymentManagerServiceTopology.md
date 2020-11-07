---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965808"
---
# <span data-ttu-id="2cdc1-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2cdc1-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="2cdc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdc1-103">更新服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-103">Updates the service topology.</span></span>

## <span data-ttu-id="2cdc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cdc1-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="2cdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="2cdc1-106">**AzDeploymentManagerServiceTopology** Cmdlet 會使用指定的服務拓朴物件更新服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="2cdc1-107">這個 Cmdlet 會傳回更新的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="2cdc1-108">示例</span><span class="sxs-lookup"><span data-stu-id="2cdc1-108">EXAMPLES</span></span>

### <span data-ttu-id="2cdc1-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2cdc1-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="2cdc1-110">這個命令會分別更新名稱和 ResourceGroup 與 $serviceTopologyObject 的 Name 和 ResourceGroupName 屬性相符的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="2cdc1-111">此命令會傳回更新的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="2cdc1-112">參數</span><span class="sxs-lookup"><span data-stu-id="2cdc1-112">PARAMETERS</span></span>

### <span data-ttu-id="2cdc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdc1-113">-DefaultProfile</span></span>
<span data-ttu-id="2cdc1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cdc1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cdc1-115">-InputObject</span></span>
<span data-ttu-id="2cdc1-116">[服務拓撲] 物件。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cdc1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2cdc1-117">-Confirm</span></span>
<span data-ttu-id="2cdc1-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdc1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdc1-119">-WhatIf</span></span>
<span data-ttu-id="2cdc1-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdc1-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdc1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdc1-122">CommonParameters</span></span>
<span data-ttu-id="2cdc1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdc1-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdc1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2cdc1-125">INPUTS</span></span>

### <span data-ttu-id="2cdc1-126">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="2cdc1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2cdc1-127">OUTPUTS</span></span>

### <span data-ttu-id="2cdc1-128">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="2cdc1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="2cdc1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2cdc1-129">NOTES</span></span>

## <span data-ttu-id="2cdc1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cdc1-130">RELATED LINKS</span></span>
