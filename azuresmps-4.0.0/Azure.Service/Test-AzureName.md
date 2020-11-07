---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967383"
---
# <span data-ttu-id="1b15d-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="1b15d-101">Test-AzureName</span></span>

## <span data-ttu-id="1b15d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b15d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b15d-103">測試是否已存在 Microsoft Azure 雲端服務名稱、儲存服務名稱或服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1b15d-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="1b15d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b15d-104">SYNTAX</span></span>

### <span data-ttu-id="1b15d-105">Services</span><span class="sxs-lookup"><span data-stu-id="1b15d-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1b15d-106">容量</span><span class="sxs-lookup"><span data-stu-id="1b15d-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1b15d-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1b15d-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1b15d-108">Web</span><span class="sxs-lookup"><span data-stu-id="1b15d-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b15d-109">說明</span><span class="sxs-lookup"><span data-stu-id="1b15d-109">DESCRIPTION</span></span>
<span data-ttu-id="1b15d-110">如果名稱存在，則 Cmdlet 會傳回 $True。</span><span class="sxs-lookup"><span data-stu-id="1b15d-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="1b15d-111">如果該名稱不存在，則會傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="1b15d-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="1b15d-112">示例</span><span class="sxs-lookup"><span data-stu-id="1b15d-112">EXAMPLES</span></span>

### <span data-ttu-id="1b15d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="1b15d-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="1b15d-114">這個命令會測試以查看「MyNameService1」是否為現有的 Microsoft Azure 雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1b15d-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="1b15d-115">範例2</span><span class="sxs-lookup"><span data-stu-id="1b15d-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="1b15d-116">這個命令會測試以查看「mystorename1」是否為現有的 Microsoft Azure 存儲服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1b15d-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="1b15d-117">範例3</span><span class="sxs-lookup"><span data-stu-id="1b15d-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="1b15d-118">這個命令會測試以查看「mynamespace」是否為現有的 Microsoft Azure 服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1b15d-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="1b15d-119">參數</span><span class="sxs-lookup"><span data-stu-id="1b15d-119">PARAMETERS</span></span>

### <span data-ttu-id="1b15d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b15d-120">-Name</span></span>
<span data-ttu-id="1b15d-121">指定要測試的服務或儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b15d-121">Specifies the name of the service or storage account to test.</span></span>

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

### <span data-ttu-id="1b15d-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1b15d-122">-Profile</span></span>
<span data-ttu-id="1b15d-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1b15d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b15d-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1b15d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b15d-125">-服務</span><span class="sxs-lookup"><span data-stu-id="1b15d-125">-Service</span></span>
<span data-ttu-id="1b15d-126">指定要測試現有的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b15d-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b15d-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1b15d-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="1b15d-128">指定要測試現有的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="1b15d-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b15d-129">儲存空間</span><span class="sxs-lookup"><span data-stu-id="1b15d-129">-Storage</span></span>
<span data-ttu-id="1b15d-130">指定要測試現有的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b15d-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b15d-131">-網站</span><span class="sxs-lookup"><span data-stu-id="1b15d-131">-Website</span></span>
<span data-ttu-id="1b15d-132">指定要測試現有的網站。</span><span class="sxs-lookup"><span data-stu-id="1b15d-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b15d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b15d-133">CommonParameters</span></span>
<span data-ttu-id="1b15d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b15d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b15d-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b15d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b15d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1b15d-136">INPUTS</span></span>

## <span data-ttu-id="1b15d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1b15d-137">OUTPUTS</span></span>

## <span data-ttu-id="1b15d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1b15d-138">NOTES</span></span>
* <span data-ttu-id="1b15d-139">節點開發人員、php 開發人員、python-開發人員</span><span class="sxs-lookup"><span data-stu-id="1b15d-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="1b15d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b15d-140">RELATED LINKS</span></span>

