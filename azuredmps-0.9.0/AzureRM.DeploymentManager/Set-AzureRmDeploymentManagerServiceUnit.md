---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442931"
---
# <span data-ttu-id="58829-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="58829-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="58829-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58829-102">SYNOPSIS</span></span>
<span data-ttu-id="58829-103">更新服務單元。</span><span class="sxs-lookup"><span data-stu-id="58829-103">Updates a service unit.</span></span>

## <span data-ttu-id="58829-104">句法</span><span class="sxs-lookup"><span data-stu-id="58829-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58829-105">說明</span><span class="sxs-lookup"><span data-stu-id="58829-105">DESCRIPTION</span></span>
<span data-ttu-id="58829-106">**AzureRmDeploymentManagerServiceUnit** Cmdlet 會使用指定的服務單元物件更新服務單元。</span><span class="sxs-lookup"><span data-stu-id="58829-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="58829-107">這個 Cmdlet 會傳回更新的服務單元物件。</span><span class="sxs-lookup"><span data-stu-id="58829-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="58829-108">示例</span><span class="sxs-lookup"><span data-stu-id="58829-108">EXAMPLES</span></span>

### <span data-ttu-id="58829-109">範例1</span><span class="sxs-lookup"><span data-stu-id="58829-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="58829-110">這個命令會分別更新 name、service name、service 拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單位。</span><span class="sxs-lookup"><span data-stu-id="58829-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="58829-111">命令會傳回更新的服務單元物件。</span><span class="sxs-lookup"><span data-stu-id="58829-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="58829-112">參數</span><span class="sxs-lookup"><span data-stu-id="58829-112">PARAMETERS</span></span>

### <span data-ttu-id="58829-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58829-113">-DefaultProfile</span></span>
<span data-ttu-id="58829-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58829-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58829-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="58829-115">-ServiceUnit</span></span>
<span data-ttu-id="58829-116">服務單位物件。</span><span class="sxs-lookup"><span data-stu-id="58829-116">The service unit object.</span></span>

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

### <span data-ttu-id="58829-117">-確認</span><span class="sxs-lookup"><span data-stu-id="58829-117">-Confirm</span></span>
<span data-ttu-id="58829-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58829-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58829-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58829-119">-WhatIf</span></span>
<span data-ttu-id="58829-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58829-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58829-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58829-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58829-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58829-122">CommonParameters</span></span>
<span data-ttu-id="58829-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58829-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58829-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58829-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58829-125">輸入</span><span class="sxs-lookup"><span data-stu-id="58829-125">INPUTS</span></span>

### <span data-ttu-id="58829-126">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="58829-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="58829-127">輸出</span><span class="sxs-lookup"><span data-stu-id="58829-127">OUTPUTS</span></span>

### <span data-ttu-id="58829-128">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="58829-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="58829-129">筆記</span><span class="sxs-lookup"><span data-stu-id="58829-129">NOTES</span></span>

## <span data-ttu-id="58829-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="58829-130">RELATED LINKS</span></span>

[<span data-ttu-id="58829-131">新-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="58829-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="58829-132">AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="58829-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="58829-133">移除-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="58829-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)