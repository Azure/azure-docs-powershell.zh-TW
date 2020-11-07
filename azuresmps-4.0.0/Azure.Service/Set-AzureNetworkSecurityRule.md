---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967246"
---
# <span data-ttu-id="5d8b2-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="5d8b2-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="5d8b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8b2-103">新增或修改網路安全性群組中的網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="5d8b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d8b2-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5d8b2-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d8b2-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8b2-106">**AzureNetworkSecurityRule** Cmdlet 會在網路安全性群組中新增或修改 Azure 網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="5d8b2-107">示例</span><span class="sxs-lookup"><span data-stu-id="5d8b2-107">EXAMPLES</span></span>

## <span data-ttu-id="5d8b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d8b2-108">PARAMETERS</span></span>

### <span data-ttu-id="5d8b2-109">-動作</span><span class="sxs-lookup"><span data-stu-id="5d8b2-109">-Action</span></span>
<span data-ttu-id="5d8b2-110">指定網路安全規則的動作。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="5d8b2-111">有效值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5d8b2-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="5d8b2-113">指定網路安全規則之目標 IP 範圍的 [無類別範圍內路由] (CIDR) 位址。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="5d8b2-114">星號 ( \* ) 會指定任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="5d8b2-115">-DestinationPortRange</span></span>
<span data-ttu-id="5d8b2-116">指定網路安全規則的目的地埠範圍。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="5d8b2-117">有效值是由從0到65535的整數所組成。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="5d8b2-118">您可以指定個別的值，或以 LowerNumber-HigherNumber 格式指定範圍。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="5d8b2-119">兩個值間有連字號。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d8b2-120">-Name</span></span>
<span data-ttu-id="5d8b2-121">指定此 Cmdlet 新增或修改之網路安全規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d8b2-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5d8b2-123">指定此 Cmdlet 修改的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="5d8b2-124">若要取得 **INetworkSecurityGroup** 物件，請使用 Get-AzureNetworkSecurityGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-125">-優先順序</span><span class="sxs-lookup"><span data-stu-id="5d8b2-125">-Priority</span></span>
<span data-ttu-id="5d8b2-126">指定網路安全規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="5d8b2-127">有效值為：從100到4096的整數。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5d8b2-128">-Profile</span></span>
<span data-ttu-id="5d8b2-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5d8b2-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="5d8b2-131">-Protocol</span></span>
<span data-ttu-id="5d8b2-132">指定網路安全規則的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="5d8b2-133">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5d8b2-133">Valid values are:</span></span> 

- <span data-ttu-id="5d8b2-134">TCP-OUT</span><span class="sxs-lookup"><span data-stu-id="5d8b2-134">TCP</span></span> 
- <span data-ttu-id="5d8b2-135">UDP-IN</span><span class="sxs-lookup"><span data-stu-id="5d8b2-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5d8b2-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="5d8b2-137">指定網路安全規則來源 IP 範圍的 CIDR 位址。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="5d8b2-138">星號 ( \* ) 會指定任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="5d8b2-139">-SourcePortRange</span></span>
<span data-ttu-id="5d8b2-140">指定網路安全規則的來源埠範圍。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="5d8b2-141">有效值是由從0到65535的整數所組成。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="5d8b2-142">您可以指定個別的值，或以 LowerNumber-HigherNumber 格式指定範圍。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="5d8b2-143">兩個值間有連字號。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-144">-類型</span><span class="sxs-lookup"><span data-stu-id="5d8b2-144">-Type</span></span>
<span data-ttu-id="5d8b2-145">指定網路安全規則的連線類型。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="5d8b2-146">有效值為： Inbound 和呼出。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8b2-147">CommonParameters</span></span>
<span data-ttu-id="5d8b2-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8b2-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d8b2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8b2-150">輸入</span><span class="sxs-lookup"><span data-stu-id="5d8b2-150">INPUTS</span></span>

## <span data-ttu-id="5d8b2-151">輸出</span><span class="sxs-lookup"><span data-stu-id="5d8b2-151">OUTPUTS</span></span>

## <span data-ttu-id="5d8b2-152">筆記</span><span class="sxs-lookup"><span data-stu-id="5d8b2-152">NOTES</span></span>

## <span data-ttu-id="5d8b2-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d8b2-153">RELATED LINKS</span></span>

[<span data-ttu-id="5d8b2-154">移除-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="5d8b2-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


