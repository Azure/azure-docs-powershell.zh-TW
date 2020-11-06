---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450700"
---
# <span data-ttu-id="98d42-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="98d42-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="98d42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98d42-102">SYNOPSIS</span></span>
<span data-ttu-id="98d42-103">新增容器服務代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="98d42-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d42-104">句法</span><span class="sxs-lookup"><span data-stu-id="98d42-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98d42-105">說明</span><span class="sxs-lookup"><span data-stu-id="98d42-105">DESCRIPTION</span></span>
<span data-ttu-id="98d42-106">**AzureRmContainerServiceAgentPoolProfile** Cmdlet 會將容器服務代理程式池設定檔新增到本機容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="98d42-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="98d42-107">示例</span><span class="sxs-lookup"><span data-stu-id="98d42-107">EXAMPLES</span></span>

### <span data-ttu-id="98d42-108">範例1：新增設定檔</span><span class="sxs-lookup"><span data-stu-id="98d42-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="98d42-109">這個命令會將容器服務代理程式池配置區新增到本機容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="98d42-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="98d42-110">參數</span><span class="sxs-lookup"><span data-stu-id="98d42-110">PARAMETERS</span></span>

### <span data-ttu-id="98d42-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="98d42-111">-ContainerService</span></span>
<span data-ttu-id="98d42-112">指定此 Cmdlet 新增代理池設定檔的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="98d42-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="98d42-113">若要取得 **ContainerService** 物件，請使用 [AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98d42-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98d42-114">-Count</span><span class="sxs-lookup"><span data-stu-id="98d42-114">-Count</span></span>
<span data-ttu-id="98d42-115">指定主機容器的代理數目。</span><span class="sxs-lookup"><span data-stu-id="98d42-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="98d42-116">此參數可接受的值為：從1到100的整數。</span><span class="sxs-lookup"><span data-stu-id="98d42-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="98d42-117">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="98d42-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d42-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="98d42-118">-DnsPrefix</span></span>
<span data-ttu-id="98d42-119">指定此 Cmdlet 用來建立此代理池之完整功能變數名稱的 DNS 前置詞。</span><span class="sxs-lookup"><span data-stu-id="98d42-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d42-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="98d42-120">-Name</span></span>
<span data-ttu-id="98d42-121">指定代理池設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="98d42-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="98d42-122">此值在訂閱和資源群組的內容中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="98d42-122">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d42-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="98d42-123">-VmSize</span></span>
<span data-ttu-id="98d42-124">指定代理程式的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="98d42-124">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d42-125">-確認</span><span class="sxs-lookup"><span data-stu-id="98d42-125">-Confirm</span></span>
<span data-ttu-id="98d42-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98d42-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d42-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d42-127">-WhatIf</span></span>
<span data-ttu-id="98d42-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98d42-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98d42-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98d42-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d42-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d42-130">CommonParameters</span></span>
<span data-ttu-id="98d42-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98d42-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d42-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98d42-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d42-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98d42-133">INPUTS</span></span>

### <span data-ttu-id="98d42-134">所有</span><span class="sxs-lookup"><span data-stu-id="98d42-134">None</span></span>
<span data-ttu-id="98d42-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="98d42-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98d42-136">輸出</span><span class="sxs-lookup"><span data-stu-id="98d42-136">OUTPUTS</span></span>

## <span data-ttu-id="98d42-137">筆記</span><span class="sxs-lookup"><span data-stu-id="98d42-137">NOTES</span></span>

## <span data-ttu-id="98d42-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="98d42-138">RELATED LINKS</span></span>

[<span data-ttu-id="98d42-139">新-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="98d42-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="98d42-140">移除-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="98d42-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
