---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285619"
---
# <span data-ttu-id="a5069-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a5069-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="a5069-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5069-102">SYNOPSIS</span></span>
<span data-ttu-id="a5069-103">新增容器服務代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="a5069-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="a5069-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5069-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5069-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5069-105">DESCRIPTION</span></span>
<span data-ttu-id="a5069-106">**AzContainerServiceAgentPoolProfile** Cmdlet 會將容器服務代理程式池設定檔新增到本機容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="a5069-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="a5069-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5069-107">EXAMPLES</span></span>

### <span data-ttu-id="a5069-108">範例1：新增設定檔</span><span class="sxs-lookup"><span data-stu-id="a5069-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="a5069-109">這個命令會將容器服務代理程式池配置區新增到本機容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="a5069-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="a5069-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5069-110">PARAMETERS</span></span>

### <span data-ttu-id="a5069-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="a5069-111">-ContainerService</span></span>
<span data-ttu-id="a5069-112">指定此 Cmdlet 新增代理池設定檔的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="a5069-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="a5069-113">若要取得 **ContainerService** 物件，請使用 [AzContainerServiceConfig](./New-AzContainerServiceConfig.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5069-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5069-114">-Count</span><span class="sxs-lookup"><span data-stu-id="a5069-114">-Count</span></span>
<span data-ttu-id="a5069-115">指定主機容器的代理數目。</span><span class="sxs-lookup"><span data-stu-id="a5069-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="a5069-116">此參數可接受的值為：從1到100的整數。</span><span class="sxs-lookup"><span data-stu-id="a5069-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="a5069-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="a5069-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5069-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5069-118">-DefaultProfile</span></span>
<span data-ttu-id="a5069-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5069-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5069-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="a5069-120">-DnsPrefix</span></span>
<span data-ttu-id="a5069-121">指定此 Cmdlet 用來建立此代理池之完整功能變數名稱的 DNS 前置詞。</span><span class="sxs-lookup"><span data-stu-id="a5069-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5069-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5069-122">-Name</span></span>
<span data-ttu-id="a5069-123">指定代理池設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5069-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="a5069-124">此值在訂閱和資源群組的內容中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a5069-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5069-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a5069-125">-VmSize</span></span>
<span data-ttu-id="a5069-126">指定代理程式的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="a5069-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5069-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a5069-127">-Confirm</span></span>
<span data-ttu-id="a5069-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5069-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5069-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5069-129">-WhatIf</span></span>
<span data-ttu-id="a5069-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5069-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5069-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5069-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5069-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5069-132">CommonParameters</span></span>
<span data-ttu-id="a5069-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5069-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5069-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5069-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5069-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a5069-135">INPUTS</span></span>

### <span data-ttu-id="a5069-136">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a5069-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="a5069-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a5069-137">System.String</span></span>

### <span data-ttu-id="a5069-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a5069-138">System.Int32</span></span>

## <span data-ttu-id="a5069-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a5069-139">OUTPUTS</span></span>

### <span data-ttu-id="a5069-140">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a5069-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a5069-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a5069-141">NOTES</span></span>

## <span data-ttu-id="a5069-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5069-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5069-143">新-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="a5069-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="a5069-144">移除-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a5069-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
