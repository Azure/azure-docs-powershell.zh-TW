---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967499"
---
# <span data-ttu-id="ddad2-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ddad2-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="ddad2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddad2-102">SYNOPSIS</span></span>
<span data-ttu-id="ddad2-103">設定 RemoteApp 集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="ddad2-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="ddad2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddad2-104">SYNTAX</span></span>

### <span data-ttu-id="ddad2-105">DescriptionOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="ddad2-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddad2-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="ddad2-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddad2-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="ddad2-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddad2-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="ddad2-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddad2-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="ddad2-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ddad2-110">說明</span><span class="sxs-lookup"><span data-stu-id="ddad2-110">DESCRIPTION</span></span>
<span data-ttu-id="ddad2-111">**AzureRemoteAppCollection** Cmdlet 會設定 Azure RemoteApp 集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="ddad2-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="ddad2-112">示例</span><span class="sxs-lookup"><span data-stu-id="ddad2-112">EXAMPLES</span></span>

## <span data-ttu-id="ddad2-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddad2-113">PARAMETERS</span></span>

### <span data-ttu-id="ddad2-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="ddad2-114">-AclLevel</span></span>
<span data-ttu-id="ddad2-115">指定集合 (ACL) 層級的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="ddad2-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="ddad2-116">此參數可接受的值為： [收集] 和 [應用程式]。</span><span class="sxs-lookup"><span data-stu-id="ddad2-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad2-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ddad2-117">-CollectionName</span></span>
<span data-ttu-id="ddad2-118">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddad2-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ddad2-119">-認證</span><span class="sxs-lookup"><span data-stu-id="ddad2-119">-Credential</span></span>
<span data-ttu-id="ddad2-120">指定擁有將 Azure RemoteApp 伺服器加入到您網域之許可權的服務帳戶認證。</span><span class="sxs-lookup"><span data-stu-id="ddad2-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="ddad2-121">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddad2-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad2-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="ddad2-122">-CustomRdpProperty</span></span>
<span data-ttu-id="ddad2-123">指定可用於設定磁片磁碟機重新導向及其他設定的自訂遠端桌面通訊協定 (RDP) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ddad2-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="ddad2-124">如需詳細資訊，請參閱[Windows Server 中的遠端桌面服務的 RDP 設定](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` 。  </span><span class="sxs-lookup"><span data-stu-id="ddad2-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad2-125">-描述</span><span class="sxs-lookup"><span data-stu-id="ddad2-125">-Description</span></span>
<span data-ttu-id="ddad2-126">指定集合的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ddad2-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad2-127">-方案</span><span class="sxs-lookup"><span data-stu-id="ddad2-127">-Plan</span></span>
<span data-ttu-id="ddad2-128">指定 Azure RemoteApp 集合的規劃，該方案定義使用限制。</span><span class="sxs-lookup"><span data-stu-id="ddad2-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="ddad2-129">使用 **AzureRemoteAppPlan** 查看可用的方案。</span><span class="sxs-lookup"><span data-stu-id="ddad2-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad2-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ddad2-130">-Profile</span></span>
<span data-ttu-id="ddad2-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ddad2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ddad2-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ddad2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddad2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddad2-133">CommonParameters</span></span>
<span data-ttu-id="ddad2-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddad2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddad2-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddad2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddad2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ddad2-136">INPUTS</span></span>

## <span data-ttu-id="ddad2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ddad2-137">OUTPUTS</span></span>

## <span data-ttu-id="ddad2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ddad2-138">NOTES</span></span>

## <span data-ttu-id="ddad2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddad2-139">RELATED LINKS</span></span>

[<span data-ttu-id="ddad2-140">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ddad2-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="ddad2-141">新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ddad2-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="ddad2-142">更新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="ddad2-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


