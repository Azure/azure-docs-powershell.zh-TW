---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968030"
---
# <span data-ttu-id="2fafb-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2fafb-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="2fafb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fafb-102">SYNOPSIS</span></span>

## <span data-ttu-id="2fafb-103">句法</span><span class="sxs-lookup"><span data-stu-id="2fafb-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2fafb-104">說明</span><span class="sxs-lookup"><span data-stu-id="2fafb-104">DESCRIPTION</span></span>

## <span data-ttu-id="2fafb-105">示例</span><span class="sxs-lookup"><span data-stu-id="2fafb-105">EXAMPLES</span></span>

### <span data-ttu-id="2fafb-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="2fafb-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2fafb-107">參數</span><span class="sxs-lookup"><span data-stu-id="2fafb-107">PARAMETERS</span></span>

### <span data-ttu-id="2fafb-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fafb-108">-InformationAction</span></span>
<span data-ttu-id="2fafb-109">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2fafb-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fafb-110">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2fafb-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fafb-111">持續</span><span class="sxs-lookup"><span data-stu-id="2fafb-111">Continue</span></span>
- <span data-ttu-id="2fafb-112">理會</span><span class="sxs-lookup"><span data-stu-id="2fafb-112">Ignore</span></span>
- <span data-ttu-id="2fafb-113">看</span><span class="sxs-lookup"><span data-stu-id="2fafb-113">Inquire</span></span>
- <span data-ttu-id="2fafb-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fafb-114">SilentlyContinue</span></span>
- <span data-ttu-id="2fafb-115">停止</span><span class="sxs-lookup"><span data-stu-id="2fafb-115">Stop</span></span>
- <span data-ttu-id="2fafb-116">封存</span><span class="sxs-lookup"><span data-stu-id="2fafb-116">Suspend</span></span>

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

### <span data-ttu-id="2fafb-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fafb-117">-InformationVariable</span></span>
<span data-ttu-id="2fafb-118">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2fafb-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2fafb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fafb-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fafb-120">-VM</span><span class="sxs-lookup"><span data-stu-id="2fafb-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fafb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fafb-121">CommonParameters</span></span>
<span data-ttu-id="2fafb-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fafb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fafb-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fafb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fafb-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2fafb-124">INPUTS</span></span>

## <span data-ttu-id="2fafb-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2fafb-125">OUTPUTS</span></span>

## <span data-ttu-id="2fafb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2fafb-126">NOTES</span></span>

## <span data-ttu-id="2fafb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fafb-127">RELATED LINKS</span></span>

[<span data-ttu-id="2fafb-128">附加 AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2fafb-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2fafb-129">移除-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2fafb-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2fafb-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2fafb-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


