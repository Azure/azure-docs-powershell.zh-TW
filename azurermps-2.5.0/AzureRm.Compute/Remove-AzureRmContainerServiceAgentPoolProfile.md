---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801741"
---
# <span data-ttu-id="05248-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05248-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="05248-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05248-102">SYNOPSIS</span></span>
<span data-ttu-id="05248-103">從容器服務移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="05248-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05248-104">句法</span><span class="sxs-lookup"><span data-stu-id="05248-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05248-105">說明</span><span class="sxs-lookup"><span data-stu-id="05248-105">DESCRIPTION</span></span>
<span data-ttu-id="05248-106">**AzureRmContainerServiceAgentPoolProfile** Cmdlet 會從容器服務中移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="05248-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="05248-107">示例</span><span class="sxs-lookup"><span data-stu-id="05248-107">EXAMPLES</span></span>

### <span data-ttu-id="05248-108">範例1：從容器服務移除設定檔</span><span class="sxs-lookup"><span data-stu-id="05248-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="05248-109">第一個命令會使用 Get-AzureRmContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="05248-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="05248-110">該命令會將服務儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="05248-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="05248-111">第二個命令會從 $Container 的容器服務中移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="05248-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="05248-112">參數</span><span class="sxs-lookup"><span data-stu-id="05248-112">PARAMETERS</span></span>

### <span data-ttu-id="05248-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="05248-113">-ContainerService</span></span>
<span data-ttu-id="05248-114">指定此 Cmdlet 從中移除代理程式組件設定檔的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="05248-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05248-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05248-115">-DefaultProfile</span></span>
<span data-ttu-id="05248-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05248-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05248-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="05248-117">-Name</span></span>
<span data-ttu-id="05248-118">指定此 Cmdlet 移除的代理池設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="05248-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05248-119">-確認</span><span class="sxs-lookup"><span data-stu-id="05248-119">-Confirm</span></span>
<span data-ttu-id="05248-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05248-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05248-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05248-121">-WhatIf</span></span>
<span data-ttu-id="05248-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05248-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05248-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05248-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05248-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05248-124">CommonParameters</span></span>
<span data-ttu-id="05248-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05248-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05248-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05248-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05248-127">輸入</span><span class="sxs-lookup"><span data-stu-id="05248-127">INPUTS</span></span>

### <span data-ttu-id="05248-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="05248-128">ContainerService</span></span>
<span data-ttu-id="05248-129">形參 "ContainerService" 接受管線中 "ContainerService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="05248-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="05248-130">輸出</span><span class="sxs-lookup"><span data-stu-id="05248-130">OUTPUTS</span></span>

### <span data-ttu-id="05248-131">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="05248-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="05248-132">筆記</span><span class="sxs-lookup"><span data-stu-id="05248-132">NOTES</span></span>

## <span data-ttu-id="05248-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="05248-133">RELATED LINKS</span></span>

[<span data-ttu-id="05248-134">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05248-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="05248-135">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05248-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

