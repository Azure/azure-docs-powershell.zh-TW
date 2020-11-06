---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: ed438e3e649d26db5b0da85b833794ad1872fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449828"
---
# <span data-ttu-id="ce71d-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce71d-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="ce71d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce71d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce71d-103">建立新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ce71d-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce71d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce71d-104">SYNTAX</span></span>

### <span data-ttu-id="ce71d-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="ce71d-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce71d-106">物件</span><span class="sxs-lookup"><span data-stu-id="ce71d-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce71d-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce71d-107">DESCRIPTION</span></span>
<span data-ttu-id="ce71d-108">**新的-AzureRmDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="ce71d-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="ce71d-109">您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce71d-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="ce71d-110">建立區域之後，請使用 New-AzureRmDnsRecordSet Cmdlet 來建立區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="ce71d-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="ce71d-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ce71d-112">示例</span><span class="sxs-lookup"><span data-stu-id="ce71d-112">EXAMPLES</span></span>

### <span data-ttu-id="ce71d-113">範例1：建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="ce71d-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ce71d-114">這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce71d-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ce71d-115">範例2：透過指定虛擬網路識別碼來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="ce71d-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="ce71d-116">這個命令會在指定的資源群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域， (指定其識別碼) ，然後將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce71d-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="ce71d-117">範例3：透過指定虛擬網路物件來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="ce71d-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="ce71d-118">這個命令會在指定的資源 (群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域，並 $ResVirtualNetwork 變數) ，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce71d-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="ce71d-119">參數</span><span class="sxs-lookup"><span data-stu-id="ce71d-119">PARAMETERS</span></span>

### <span data-ttu-id="ce71d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce71d-120">-DefaultProfile</span></span>
<span data-ttu-id="ce71d-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce71d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce71d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce71d-122">-Name</span></span>
<span data-ttu-id="ce71d-123">指定要建立之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce71d-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="ce71d-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce71d-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="ce71d-125">將在這個 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="ce71d-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ce71d-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="ce71d-127">將在這個 DNS 區域中登錄虛擬機器主機名稱記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="ce71d-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce71d-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="ce71d-129">可解析此 DNS 區域中之記錄的虛擬網路清單，只能供私人區域使用。</span><span class="sxs-lookup"><span data-stu-id="ce71d-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ce71d-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="ce71d-131">可解析此 DNS 區域中之記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="ce71d-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce71d-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce71d-133">指定要在其中建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ce71d-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="ce71d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce71d-134">-Tag</span></span>
<span data-ttu-id="ce71d-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ce71d-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ce71d-136">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ce71d-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="ce71d-137">-ZoneType</span></span>
<span data-ttu-id="ce71d-138">該區域的類型為 [公用] 或 [私人]。</span><span class="sxs-lookup"><span data-stu-id="ce71d-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="ce71d-139">在 DNS 階層中使用的公用 DNS 服務平面上提供不含類型或屬於 Public 類型的區域。</span><span class="sxs-lookup"><span data-stu-id="ce71d-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="ce71d-140">具有私人類型的區域只會與一組關聯的虛擬網路一起顯示 (這項功能在預覽) 中。</span><span class="sxs-lookup"><span data-stu-id="ce71d-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="ce71d-141">此屬性無法針對區域進行變更。</span><span class="sxs-lookup"><span data-stu-id="ce71d-141">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-142">-確認</span><span class="sxs-lookup"><span data-stu-id="ce71d-142">-Confirm</span></span>
<span data-ttu-id="ce71d-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce71d-144">-WhatIf</span></span>
<span data-ttu-id="ce71d-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce71d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce71d-146">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce71d-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce71d-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce71d-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce71d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce71d-148">CommonParameters</span></span>
<span data-ttu-id="ce71d-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce71d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce71d-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce71d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce71d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="ce71d-151">INPUTS</span></span>

### <span data-ttu-id="ce71d-152">System.object</span><span class="sxs-lookup"><span data-stu-id="ce71d-152">System.String</span></span>

### <span data-ttu-id="ce71d-153">"ZoneType" 1 [[2.1.0.0]。 Dns，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]] （"）]</span><span class="sxs-lookup"><span data-stu-id="ce71d-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ce71d-154">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ce71d-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ce71d-155">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ce71d-155">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ce71d-156">[System.object]. 清單 ' 1 [IResourceReference]。 common. Network、Version = 1.0.0.0、Culture = 中性、PublicKeyToken = null]]。）），）的區域性 = 非特定語言。</span><span class="sxs-lookup"><span data-stu-id="ce71d-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ce71d-157">輸出</span><span class="sxs-lookup"><span data-stu-id="ce71d-157">OUTPUTS</span></span>

### <span data-ttu-id="ce71d-158">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="ce71d-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="ce71d-159">筆記</span><span class="sxs-lookup"><span data-stu-id="ce71d-159">NOTES</span></span>
<span data-ttu-id="ce71d-160">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ce71d-161">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ce71d-162">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ce71d-163">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce71d-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ce71d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce71d-164">RELATED LINKS</span></span>

[<span data-ttu-id="ce71d-165">AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce71d-165">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="ce71d-166">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ce71d-166">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ce71d-167">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="ce71d-167">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
