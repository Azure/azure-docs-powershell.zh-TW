---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967239"
---
# <span data-ttu-id="0b319-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b319-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="0b319-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b319-102">SYNOPSIS</span></span>

## <span data-ttu-id="0b319-103">句法</span><span class="sxs-lookup"><span data-stu-id="0b319-103">SYNTAX</span></span>

### <span data-ttu-id="0b319-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b319-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0b319-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b319-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b319-106">說明</span><span class="sxs-lookup"><span data-stu-id="0b319-106">DESCRIPTION</span></span>

## <span data-ttu-id="0b319-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b319-107">EXAMPLES</span></span>

### <span data-ttu-id="0b319-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="0b319-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0b319-109">參數</span><span class="sxs-lookup"><span data-stu-id="0b319-109">PARAMETERS</span></span>

### <span data-ttu-id="0b319-110">-停用</span><span class="sxs-lookup"><span data-stu-id="0b319-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b319-111">-啟用</span><span class="sxs-lookup"><span data-stu-id="0b319-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b319-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0b319-112">-InformationAction</span></span>
<span data-ttu-id="0b319-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0b319-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b319-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0b319-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b319-115">持續</span><span class="sxs-lookup"><span data-stu-id="0b319-115">Continue</span></span>
- <span data-ttu-id="0b319-116">理會</span><span class="sxs-lookup"><span data-stu-id="0b319-116">Ignore</span></span>
- <span data-ttu-id="0b319-117">看</span><span class="sxs-lookup"><span data-stu-id="0b319-117">Inquire</span></span>
- <span data-ttu-id="0b319-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0b319-118">SilentlyContinue</span></span>
- <span data-ttu-id="0b319-119">停止</span><span class="sxs-lookup"><span data-stu-id="0b319-119">Stop</span></span>
- <span data-ttu-id="0b319-120">封存</span><span class="sxs-lookup"><span data-stu-id="0b319-120">Suspend</span></span>

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

### <span data-ttu-id="0b319-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0b319-121">-InformationVariable</span></span>
<span data-ttu-id="0b319-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0b319-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0b319-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0b319-123">-Profile</span></span>
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

### <span data-ttu-id="0b319-124">-VM</span><span class="sxs-lookup"><span data-stu-id="0b319-124">-VM</span></span>
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

### <span data-ttu-id="0b319-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b319-125">CommonParameters</span></span>
<span data-ttu-id="0b319-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b319-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b319-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b319-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b319-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0b319-128">INPUTS</span></span>

## <span data-ttu-id="0b319-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0b319-129">OUTPUTS</span></span>

## <span data-ttu-id="0b319-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0b319-130">NOTES</span></span>

## <span data-ttu-id="0b319-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b319-131">RELATED LINKS</span></span>

