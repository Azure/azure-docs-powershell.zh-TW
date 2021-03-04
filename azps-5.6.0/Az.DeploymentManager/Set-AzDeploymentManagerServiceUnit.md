---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 24c682faf725fd53e3b78e85c316318300ecbb62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904445"
---
# <span data-ttu-id="30b99-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="30b99-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="30b99-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30b99-102">SYNOPSIS</span></span>
<span data-ttu-id="30b99-103">更新服務單位。</span><span class="sxs-lookup"><span data-stu-id="30b99-103">Updates the service unit.</span></span>

## <span data-ttu-id="30b99-104">語法</span><span class="sxs-lookup"><span data-stu-id="30b99-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30b99-105">描述</span><span class="sxs-lookup"><span data-stu-id="30b99-105">DESCRIPTION</span></span>
<span data-ttu-id="30b99-106">**Set-AzDeploymentManagerServiceUnit** Cmdlet 會以指定的服務單位物件更新服務單位。</span><span class="sxs-lookup"><span data-stu-id="30b99-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="30b99-107">Cmdlet 會返回更新的服務單位物件。</span><span class="sxs-lookup"><span data-stu-id="30b99-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="30b99-108">例子</span><span class="sxs-lookup"><span data-stu-id="30b99-108">EXAMPLES</span></span>

### <span data-ttu-id="30b99-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="30b99-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="30b99-110">此命令會更新服務單位，其名稱、服務名稱、服務拓撲名稱及 ResourceGroup 分別符合服務名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性$serviceUnitObject名稱。</span><span class="sxs-lookup"><span data-stu-id="30b99-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="30b99-111">該命令會返回更新的服務單位物件。</span><span class="sxs-lookup"><span data-stu-id="30b99-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="30b99-112">參數</span><span class="sxs-lookup"><span data-stu-id="30b99-112">PARAMETERS</span></span>

### <span data-ttu-id="30b99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b99-113">-DefaultProfile</span></span>
<span data-ttu-id="30b99-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30b99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30b99-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30b99-115">-InputObject</span></span>
<span data-ttu-id="30b99-116">服務單位物件。</span><span class="sxs-lookup"><span data-stu-id="30b99-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30b99-117">-確認</span><span class="sxs-lookup"><span data-stu-id="30b99-117">-Confirm</span></span>
<span data-ttu-id="30b99-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30b99-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30b99-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30b99-119">-WhatIf</span></span>
<span data-ttu-id="30b99-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30b99-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30b99-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30b99-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30b99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b99-122">CommonParameters</span></span>
<span data-ttu-id="30b99-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30b99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b99-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30b99-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b99-125">輸入</span><span class="sxs-lookup"><span data-stu-id="30b99-125">INPUTS</span></span>

### <span data-ttu-id="30b99-126">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="30b99-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="30b99-127">輸出</span><span class="sxs-lookup"><span data-stu-id="30b99-127">OUTPUTS</span></span>

### <span data-ttu-id="30b99-128">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="30b99-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="30b99-129">筆記</span><span class="sxs-lookup"><span data-stu-id="30b99-129">NOTES</span></span>

## <span data-ttu-id="30b99-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="30b99-130">RELATED LINKS</span></span>
