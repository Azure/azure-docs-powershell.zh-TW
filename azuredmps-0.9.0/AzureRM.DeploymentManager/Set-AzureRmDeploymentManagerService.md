---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442460"
---
# <span data-ttu-id="b77f3-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b77f3-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="b77f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b77f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b77f3-103">更新服務拓撲中的服務。</span><span class="sxs-lookup"><span data-stu-id="b77f3-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="b77f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b77f3-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="b77f3-105">DESCRIPTION</span></span>
<span data-ttu-id="b77f3-106">**AzureRmDeploymentManagerService** Cmdlet 會使用指定的服務物件更新服務。</span><span class="sxs-lookup"><span data-stu-id="b77f3-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="b77f3-107">這個 Cmdlet 會傳回更新的服務物件。</span><span class="sxs-lookup"><span data-stu-id="b77f3-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="b77f3-108">示例</span><span class="sxs-lookup"><span data-stu-id="b77f3-108">EXAMPLES</span></span>

### <span data-ttu-id="b77f3-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b77f3-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="b77f3-110">這個命令會分別更新 name、service 拓朴名稱和 ResourceGroup 的服務，分別與 $serviceObject 的 Name、ServiceTopologyName 和 ResourceGroupName 屬性相符。</span><span class="sxs-lookup"><span data-stu-id="b77f3-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="b77f3-111">該服務將會更新為 $serviceObject 中設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="b77f3-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="b77f3-112">參數</span><span class="sxs-lookup"><span data-stu-id="b77f3-112">PARAMETERS</span></span>

### <span data-ttu-id="b77f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77f3-113">-DefaultProfile</span></span>
<span data-ttu-id="b77f3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b77f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b77f3-115">-服務</span><span class="sxs-lookup"><span data-stu-id="b77f3-115">-Service</span></span>
<span data-ttu-id="b77f3-116">服務物件。</span><span class="sxs-lookup"><span data-stu-id="b77f3-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77f3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b77f3-117">-Confirm</span></span>
<span data-ttu-id="b77f3-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b77f3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77f3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77f3-119">-WhatIf</span></span>
<span data-ttu-id="b77f3-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b77f3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b77f3-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b77f3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77f3-122">CommonParameters</span></span>
<span data-ttu-id="b77f3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b77f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77f3-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b77f3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77f3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b77f3-125">INPUTS</span></span>

### <span data-ttu-id="b77f3-126">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="b77f3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b77f3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b77f3-127">OUTPUTS</span></span>

### <span data-ttu-id="b77f3-128">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="b77f3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b77f3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b77f3-129">NOTES</span></span>

## <span data-ttu-id="b77f3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b77f3-130">RELATED LINKS</span></span>

[<span data-ttu-id="b77f3-131">新-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b77f3-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="b77f3-132">AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b77f3-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="b77f3-133">移除-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b77f3-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)