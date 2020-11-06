---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 097377cd1ca4cb4be4fe62e2008f899c05c194fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455995"
---
# <span data-ttu-id="f3330-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3330-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f3330-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3330-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3330-103">句法</span><span class="sxs-lookup"><span data-stu-id="f3330-103">SYNTAX</span></span>

### <span data-ttu-id="f3330-104">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f3330-104">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3330-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3330-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3330-106">說明</span><span class="sxs-lookup"><span data-stu-id="f3330-106">DESCRIPTION</span></span>

## <span data-ttu-id="f3330-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3330-107">EXAMPLES</span></span>

### <span data-ttu-id="f3330-108">1：新增</span><span class="sxs-lookup"><span data-stu-id="f3330-108">1: New</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="f3330-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3330-109">PARAMETERS</span></span>

### <span data-ttu-id="f3330-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f3330-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3330-111">-DefaultProfile</span></span>
<span data-ttu-id="f3330-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3330-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3330-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f3330-113">-EnableFloatingIP</span></span>
<span data-ttu-id="f3330-114">針對設定 SQL AlwaysOn 可用性群組所需的浮動 IP 功能，配置虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="f3330-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="f3330-115">使用 SQL server 中的 SQL AlwaysOn 可用性群組時，此設定是必要的。</span><span class="sxs-lookup"><span data-stu-id="f3330-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="f3330-116">在您建立端點之後，就無法變更此設定。</span><span class="sxs-lookup"><span data-stu-id="f3330-116">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f3330-117">-EnableTcpReset</span></span>
<span data-ttu-id="f3330-118">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="f3330-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f3330-119">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="f3330-119">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3330-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f3330-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="f3330-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="f3330-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f3330-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f3330-125">TCP 空閒連線的超時時間。</span><span class="sxs-lookup"><span data-stu-id="f3330-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="f3330-126">此值可設定為4到30分鐘。</span><span class="sxs-lookup"><span data-stu-id="f3330-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="f3330-127">預設值為4分鐘。</span><span class="sxs-lookup"><span data-stu-id="f3330-127">The default value is 4 minutes.</span></span> <span data-ttu-id="f3330-128">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="f3330-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3330-129">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3330-130">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f3330-130">-Protocol</span></span>
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

### <span data-ttu-id="f3330-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f3330-131">-Confirm</span></span>
<span data-ttu-id="f3330-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3330-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3330-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3330-133">-WhatIf</span></span>
<span data-ttu-id="f3330-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3330-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3330-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3330-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3330-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3330-136">CommonParameters</span></span>
<span data-ttu-id="f3330-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3330-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3330-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3330-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3330-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f3330-139">INPUTS</span></span>

### <span data-ttu-id="f3330-140">所有</span><span class="sxs-lookup"><span data-stu-id="f3330-140">None</span></span>

## <span data-ttu-id="f3330-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f3330-141">OUTPUTS</span></span>

### <span data-ttu-id="f3330-142">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3330-142">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="f3330-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f3330-143">NOTES</span></span>

## <span data-ttu-id="f3330-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3330-144">RELATED LINKS</span></span>
