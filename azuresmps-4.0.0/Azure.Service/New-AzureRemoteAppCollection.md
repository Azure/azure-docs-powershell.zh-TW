---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967442"
---
# <span data-ttu-id="131f6-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="131f6-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="131f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="131f6-102">SYNOPSIS</span></span>
<span data-ttu-id="131f6-103">建立 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="131f6-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="131f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="131f6-104">SYNTAX</span></span>

### <span data-ttu-id="131f6-105">AllParameterSets (預設) </span><span class="sxs-lookup"><span data-stu-id="131f6-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="131f6-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="131f6-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="131f6-107">說明</span><span class="sxs-lookup"><span data-stu-id="131f6-107">DESCRIPTION</span></span>
<span data-ttu-id="131f6-108">**新的-AzureRemoteAppCollection** Cmdlet 會建立 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="131f6-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="131f6-109">示例</span><span class="sxs-lookup"><span data-stu-id="131f6-109">EXAMPLES</span></span>

### <span data-ttu-id="131f6-110">範例1：建立集合</span><span class="sxs-lookup"><span data-stu-id="131f6-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="131f6-111">這個命令會建立 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="131f6-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="131f6-112">範例2：使用認證建立集合</span><span class="sxs-lookup"><span data-stu-id="131f6-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="131f6-113">這個命令會使用 **取得認證** Cmdlet 的認證來建立 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="131f6-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="131f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="131f6-114">PARAMETERS</span></span>

### <span data-ttu-id="131f6-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="131f6-115">-CollectionName</span></span>
<span data-ttu-id="131f6-116">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="131f6-116">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-117">-認證</span><span class="sxs-lookup"><span data-stu-id="131f6-117">-Credential</span></span>
<span data-ttu-id="131f6-118">指定擁有將 Azure RemoteApp 伺服器加入到您網域之許可權的服務帳戶認證。</span><span class="sxs-lookup"><span data-stu-id="131f6-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="131f6-119">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131f6-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="131f6-120">-CustomRdpProperty</span></span>
<span data-ttu-id="131f6-121">指定 [自訂遠端桌面 Protocal] (RDP) 屬性，可用來設定磁片磁碟機重新導向及其他設定。</span><span class="sxs-lookup"><span data-stu-id="131f6-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="131f6-122">如需詳細資訊，請參閱[Windows Server 中的遠端桌面服務的 RDP 設定](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` 。  </span><span class="sxs-lookup"><span data-stu-id="131f6-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-123">-描述</span><span class="sxs-lookup"><span data-stu-id="131f6-123">-Description</span></span>
<span data-ttu-id="131f6-124">指定物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="131f6-124">Specifies a short description for the object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="131f6-125">-DnsServers</span></span>
<span data-ttu-id="131f6-126">指定以逗號分隔的 DNS 伺服器 IPv4 地址清單。</span><span class="sxs-lookup"><span data-stu-id="131f6-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-127">-網域</span><span class="sxs-lookup"><span data-stu-id="131f6-127">-Domain</span></span>
<span data-ttu-id="131f6-128">指定要加入 RD 工作階段主機伺服器之 Active Directory 網域服務網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="131f6-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="131f6-129">-ImageName</span></span>
<span data-ttu-id="131f6-130">指定 Azure RemoteApp 範本映射的名稱。</span><span class="sxs-lookup"><span data-stu-id="131f6-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-131">-位置</span><span class="sxs-lookup"><span data-stu-id="131f6-131">-Location</span></span>
<span data-ttu-id="131f6-132">指定集合的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="131f6-132">Specifies the Azure region of the collection.</span></span>

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

### <span data-ttu-id="131f6-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="131f6-133">-OrganizationalUnit</span></span>
<span data-ttu-id="131f6-134">指定要加入 RD 工作階段主機伺服器之組織單位 (OU) 的名稱，例如 OU = MyOu、DC = MyDomain、DC = ParentDomain、DC = com。</span><span class="sxs-lookup"><span data-stu-id="131f6-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="131f6-135">OU 和 DC 等屬性必須是大寫。</span><span class="sxs-lookup"><span data-stu-id="131f6-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="131f6-136">建立集合之後，就無法變更 OU。</span><span class="sxs-lookup"><span data-stu-id="131f6-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-137">-方案</span><span class="sxs-lookup"><span data-stu-id="131f6-137">-Plan</span></span>
<span data-ttu-id="131f6-138">指定 Azure RemoteApp 集合的方案，這可能會定義使用限制。</span><span class="sxs-lookup"><span data-stu-id="131f6-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="131f6-139">使用 **AzureRemoteAppPlan** 查看可用的方案。</span><span class="sxs-lookup"><span data-stu-id="131f6-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-140">-設定檔</span><span class="sxs-lookup"><span data-stu-id="131f6-140">-Profile</span></span>
<span data-ttu-id="131f6-141">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="131f6-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="131f6-142">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="131f6-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="131f6-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="131f6-143">-ResourceType</span></span>
<span data-ttu-id="131f6-144">指定集合的資源類型。</span><span class="sxs-lookup"><span data-stu-id="131f6-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="131f6-145">此參數可接受的值為： [App] 或 [桌面]。</span><span class="sxs-lookup"><span data-stu-id="131f6-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="131f6-146">-SubnetName</span></span>
<span data-ttu-id="131f6-147">指定虛擬網路中要用來建立 Azure RemoteApp 集合之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="131f6-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="131f6-148">-VNetName</span></span>
<span data-ttu-id="131f6-149">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="131f6-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131f6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131f6-150">CommonParameters</span></span>
<span data-ttu-id="131f6-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="131f6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131f6-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="131f6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131f6-153">輸入</span><span class="sxs-lookup"><span data-stu-id="131f6-153">INPUTS</span></span>

## <span data-ttu-id="131f6-154">輸出</span><span class="sxs-lookup"><span data-stu-id="131f6-154">OUTPUTS</span></span>

## <span data-ttu-id="131f6-155">筆記</span><span class="sxs-lookup"><span data-stu-id="131f6-155">NOTES</span></span>

## <span data-ttu-id="131f6-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="131f6-156">RELATED LINKS</span></span>

[<span data-ttu-id="131f6-157">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="131f6-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="131f6-158">AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="131f6-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="131f6-159">移除-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="131f6-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="131f6-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="131f6-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="131f6-161">更新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="131f6-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


