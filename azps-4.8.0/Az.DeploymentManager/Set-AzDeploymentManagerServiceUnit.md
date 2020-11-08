---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136461"
---
# <span data-ttu-id="08282-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="08282-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="08282-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08282-102">SYNOPSIS</span></span>
<span data-ttu-id="08282-103">更新服務單元。</span><span class="sxs-lookup"><span data-stu-id="08282-103">Updates the service unit.</span></span>

## <span data-ttu-id="08282-104">句法</span><span class="sxs-lookup"><span data-stu-id="08282-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08282-105">說明</span><span class="sxs-lookup"><span data-stu-id="08282-105">DESCRIPTION</span></span>
<span data-ttu-id="08282-106">**AzDeploymentManagerServiceUnit** Cmdlet 會使用指定的服務單元物件更新服務單元。</span><span class="sxs-lookup"><span data-stu-id="08282-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="08282-107">這個 Cmdlet 會傳回更新的服務單元物件。</span><span class="sxs-lookup"><span data-stu-id="08282-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="08282-108">示例</span><span class="sxs-lookup"><span data-stu-id="08282-108">EXAMPLES</span></span>

### <span data-ttu-id="08282-109">範例1</span><span class="sxs-lookup"><span data-stu-id="08282-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="08282-110">這個命令會分別更新 name、service name、service 拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單位。</span><span class="sxs-lookup"><span data-stu-id="08282-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="08282-111">命令會傳回更新的服務單元物件。</span><span class="sxs-lookup"><span data-stu-id="08282-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="08282-112">參數</span><span class="sxs-lookup"><span data-stu-id="08282-112">PARAMETERS</span></span>

### <span data-ttu-id="08282-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08282-113">-DefaultProfile</span></span>
<span data-ttu-id="08282-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08282-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08282-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08282-115">-InputObject</span></span>
<span data-ttu-id="08282-116">服務單位物件。</span><span class="sxs-lookup"><span data-stu-id="08282-116">The service unit object.</span></span>

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

### <span data-ttu-id="08282-117">-確認</span><span class="sxs-lookup"><span data-stu-id="08282-117">-Confirm</span></span>
<span data-ttu-id="08282-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08282-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08282-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08282-119">-WhatIf</span></span>
<span data-ttu-id="08282-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08282-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08282-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08282-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08282-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08282-122">CommonParameters</span></span>
<span data-ttu-id="08282-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08282-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08282-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08282-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08282-125">輸入</span><span class="sxs-lookup"><span data-stu-id="08282-125">INPUTS</span></span>

### <span data-ttu-id="08282-126">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="08282-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="08282-127">輸出</span><span class="sxs-lookup"><span data-stu-id="08282-127">OUTPUTS</span></span>

### <span data-ttu-id="08282-128">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="08282-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="08282-129">筆記</span><span class="sxs-lookup"><span data-stu-id="08282-129">NOTES</span></span>

## <span data-ttu-id="08282-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="08282-130">RELATED LINKS</span></span>