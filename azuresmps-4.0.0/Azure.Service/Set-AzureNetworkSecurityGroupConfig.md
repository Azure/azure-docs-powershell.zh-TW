---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967202"
---
# <span data-ttu-id="4e17e-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="4e17e-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="4e17e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e17e-102">SYNOPSIS</span></span>

## <span data-ttu-id="4e17e-103">句法</span><span class="sxs-lookup"><span data-stu-id="4e17e-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e17e-104">說明</span><span class="sxs-lookup"><span data-stu-id="4e17e-104">DESCRIPTION</span></span>

## <span data-ttu-id="4e17e-105">示例</span><span class="sxs-lookup"><span data-stu-id="4e17e-105">EXAMPLES</span></span>

### <span data-ttu-id="4e17e-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="4e17e-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4e17e-107">參數</span><span class="sxs-lookup"><span data-stu-id="4e17e-107">PARAMETERS</span></span>

### <span data-ttu-id="4e17e-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4e17e-108">-InformationAction</span></span>
<span data-ttu-id="4e17e-109">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="4e17e-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4e17e-110">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4e17e-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e17e-111">持續</span><span class="sxs-lookup"><span data-stu-id="4e17e-111">Continue</span></span>
- <span data-ttu-id="4e17e-112">理會</span><span class="sxs-lookup"><span data-stu-id="4e17e-112">Ignore</span></span>
- <span data-ttu-id="4e17e-113">看</span><span class="sxs-lookup"><span data-stu-id="4e17e-113">Inquire</span></span>
- <span data-ttu-id="4e17e-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4e17e-114">SilentlyContinue</span></span>
- <span data-ttu-id="4e17e-115">停止</span><span class="sxs-lookup"><span data-stu-id="4e17e-115">Stop</span></span>
- <span data-ttu-id="4e17e-116">封存</span><span class="sxs-lookup"><span data-stu-id="4e17e-116">Suspend</span></span>

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

### <span data-ttu-id="4e17e-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4e17e-117">-InformationVariable</span></span>
<span data-ttu-id="4e17e-118">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="4e17e-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4e17e-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="4e17e-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="4e17e-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4e17e-120">-Profile</span></span>
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

### <span data-ttu-id="4e17e-121">-VM</span><span class="sxs-lookup"><span data-stu-id="4e17e-121">-VM</span></span>
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

### <span data-ttu-id="4e17e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e17e-122">CommonParameters</span></span>
<span data-ttu-id="4e17e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e17e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e17e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e17e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e17e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4e17e-125">INPUTS</span></span>

## <span data-ttu-id="4e17e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4e17e-126">OUTPUTS</span></span>

## <span data-ttu-id="4e17e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4e17e-127">NOTES</span></span>

## <span data-ttu-id="4e17e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e17e-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e17e-129">移除-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="4e17e-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


