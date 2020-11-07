---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624093"
---
# <span data-ttu-id="d0284-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0284-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="d0284-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0284-102">SYNOPSIS</span></span>
<span data-ttu-id="d0284-103">建立新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="d0284-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0284-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0284-104">SYNTAX</span></span>

### <span data-ttu-id="d0284-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="d0284-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0284-106">物件</span><span class="sxs-lookup"><span data-stu-id="d0284-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0284-107">說明</span><span class="sxs-lookup"><span data-stu-id="d0284-107">DESCRIPTION</span></span>
<span data-ttu-id="d0284-108">**新的-AzureRmDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="d0284-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="d0284-109">您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0284-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="d0284-110">建立區域之後，請使用 New-AzureRmDnsRecordSet Cmdlet 來建立區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d0284-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="d0284-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d0284-112">示例</span><span class="sxs-lookup"><span data-stu-id="d0284-112">EXAMPLES</span></span>

### <span data-ttu-id="d0284-113">範例1：建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="d0284-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d0284-114">這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0284-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d0284-115">範例2：透過指定虛擬網路識別碼來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="d0284-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="d0284-116">這個命令會在指定的資源群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域， (指定其識別碼) ，然後將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0284-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d0284-117">範例3：透過指定虛擬網路物件來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="d0284-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="d0284-118">這個命令會在指定的資源 (群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域，並 $ResVirtualNetwork 變數) ，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0284-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="d0284-119">參數</span><span class="sxs-lookup"><span data-stu-id="d0284-119">PARAMETERS</span></span>

### <span data-ttu-id="d0284-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0284-120">-DefaultProfile</span></span>
<span data-ttu-id="d0284-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d0284-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0284-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0284-122">-Name</span></span>
<span data-ttu-id="d0284-123">指定要建立之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0284-123">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0284-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="d0284-125">將在這個 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="d0284-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="d0284-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d0284-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="d0284-127">將在這個 DNS 區域中登錄虛擬機器主機名稱記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="d0284-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="d0284-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0284-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="d0284-129">可解析此 DNS 區域中之記錄的虛擬網路清單，只能供私人區域使用。</span><span class="sxs-lookup"><span data-stu-id="d0284-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="d0284-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d0284-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="d0284-131">可解析此 DNS 區域中之記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="d0284-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="d0284-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0284-132">-ResourceGroupName</span></span>
<span data-ttu-id="d0284-133">指定要在其中建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d0284-133">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0284-134">-Tag</span></span>
<span data-ttu-id="d0284-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d0284-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0284-136">例如：</span><span class="sxs-lookup"><span data-stu-id="d0284-136">For example:</span></span>

<span data-ttu-id="d0284-137">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d0284-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-138">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="d0284-138">-ZoneType</span></span>
<span data-ttu-id="d0284-139">該區域的類型為 [公用] 或 [私人]。</span><span class="sxs-lookup"><span data-stu-id="d0284-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="d0284-140">在 DNS 階層中使用的公用 DNS 服務平面上提供不含類型或屬於 Public 類型的區域。</span><span class="sxs-lookup"><span data-stu-id="d0284-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="d0284-141">具有私人類型的區域只會與一組關聯的虛擬網路一起顯示 (這項功能在預覽) 中。</span><span class="sxs-lookup"><span data-stu-id="d0284-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="d0284-142">此屬性無法針對區域進行變更。</span><span class="sxs-lookup"><span data-stu-id="d0284-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-143">-確認</span><span class="sxs-lookup"><span data-stu-id="d0284-143">-Confirm</span></span>
<span data-ttu-id="d0284-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0284-145">-WhatIf</span></span>
<span data-ttu-id="d0284-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0284-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0284-147">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0284-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0284-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0284-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0284-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0284-149">CommonParameters</span></span>
<span data-ttu-id="d0284-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0284-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0284-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0284-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0284-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d0284-152">INPUTS</span></span>

### <span data-ttu-id="d0284-153">所有</span><span class="sxs-lookup"><span data-stu-id="d0284-153">None</span></span>
<span data-ttu-id="d0284-154">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0284-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="d0284-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d0284-155">OUTPUTS</span></span>

### <span data-ttu-id="d0284-156">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="d0284-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d0284-157">這個 Cmdlet 會傳回代表新的 DNS 區域的 DnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="d0284-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="d0284-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d0284-158">NOTES</span></span>
<span data-ttu-id="d0284-159">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d0284-160">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="d0284-161">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d0284-162">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0284-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d0284-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0284-163">RELATED LINKS</span></span>

[<span data-ttu-id="d0284-164">AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0284-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="d0284-165">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d0284-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d0284-166">移除-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d0284-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
