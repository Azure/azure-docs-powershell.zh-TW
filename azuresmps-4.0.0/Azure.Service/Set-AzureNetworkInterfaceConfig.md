---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967251"
---
# <span data-ttu-id="3f57e-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3f57e-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="3f57e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f57e-102">SYNOPSIS</span></span>

## <span data-ttu-id="3f57e-103">句法</span><span class="sxs-lookup"><span data-stu-id="3f57e-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f57e-104">說明</span><span class="sxs-lookup"><span data-stu-id="3f57e-104">DESCRIPTION</span></span>

## <span data-ttu-id="3f57e-105">示例</span><span class="sxs-lookup"><span data-stu-id="3f57e-105">EXAMPLES</span></span>

### <span data-ttu-id="3f57e-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="3f57e-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3f57e-107">參數</span><span class="sxs-lookup"><span data-stu-id="3f57e-107">PARAMETERS</span></span>

### <span data-ttu-id="3f57e-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f57e-108">-InformationAction</span></span>
<span data-ttu-id="3f57e-109">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3f57e-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f57e-110">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3f57e-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f57e-111">持續</span><span class="sxs-lookup"><span data-stu-id="3f57e-111">Continue</span></span>
- <span data-ttu-id="3f57e-112">理會</span><span class="sxs-lookup"><span data-stu-id="3f57e-112">Ignore</span></span>
- <span data-ttu-id="3f57e-113">看</span><span class="sxs-lookup"><span data-stu-id="3f57e-113">Inquire</span></span>
- <span data-ttu-id="3f57e-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f57e-114">SilentlyContinue</span></span>
- <span data-ttu-id="3f57e-115">停止</span><span class="sxs-lookup"><span data-stu-id="3f57e-115">Stop</span></span>
- <span data-ttu-id="3f57e-116">封存</span><span class="sxs-lookup"><span data-stu-id="3f57e-116">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f57e-117">-InformationVariable</span></span>
<span data-ttu-id="3f57e-118">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3f57e-118">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="3f57e-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f57e-120">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3f57e-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3f57e-122">-Profile</span></span>
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

### <span data-ttu-id="3f57e-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f57e-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3f57e-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3f57e-125">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f57e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f57e-126">CommonParameters</span></span>
<span data-ttu-id="3f57e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f57e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f57e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f57e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f57e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3f57e-129">INPUTS</span></span>

## <span data-ttu-id="3f57e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3f57e-130">OUTPUTS</span></span>

## <span data-ttu-id="3f57e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3f57e-131">NOTES</span></span>

## <span data-ttu-id="3f57e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f57e-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f57e-133">附加 AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3f57e-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="3f57e-134">AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3f57e-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="3f57e-135">移除-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="3f57e-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


