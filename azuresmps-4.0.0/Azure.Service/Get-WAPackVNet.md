---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967709"
---
# <span data-ttu-id="52f95-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="52f95-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="52f95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52f95-102">SYNOPSIS</span></span>
<span data-ttu-id="52f95-103">取得虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="52f95-103">Gets virtual networks.</span></span>

## <span data-ttu-id="52f95-104">句法</span><span class="sxs-lookup"><span data-stu-id="52f95-104">SYNTAX</span></span>

### <span data-ttu-id="52f95-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="52f95-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52f95-106">FromId</span><span class="sxs-lookup"><span data-stu-id="52f95-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52f95-107">FromName</span><span class="sxs-lookup"><span data-stu-id="52f95-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52f95-108">說明</span><span class="sxs-lookup"><span data-stu-id="52f95-108">DESCRIPTION</span></span>
<span data-ttu-id="52f95-109">**WAPackVNet** Cmdlet 會取得虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="52f95-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="52f95-110">示例</span><span class="sxs-lookup"><span data-stu-id="52f95-110">EXAMPLES</span></span>

### <span data-ttu-id="52f95-111">範例1：取得所有虛擬網路</span><span class="sxs-lookup"><span data-stu-id="52f95-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="52f95-112">這個命令會取得所有虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="52f95-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="52f95-113">範例2：使用識別碼取得虛擬網路</span><span class="sxs-lookup"><span data-stu-id="52f95-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="52f95-114">這個命令會取得具有指定識別碼的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="52f95-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="52f95-115">範例3：使用名稱取得虛擬網路</span><span class="sxs-lookup"><span data-stu-id="52f95-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="52f95-116">這個命令會取得名為 ContosoVNet08 的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="52f95-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="52f95-117">參數</span><span class="sxs-lookup"><span data-stu-id="52f95-117">PARAMETERS</span></span>

### <span data-ttu-id="52f95-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="52f95-118">-ID</span></span>
<span data-ttu-id="52f95-119">指定虛擬網路的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="52f95-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f95-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="52f95-120">-Name</span></span>
<span data-ttu-id="52f95-121">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="52f95-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f95-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="52f95-122">-Profile</span></span>
<span data-ttu-id="52f95-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="52f95-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52f95-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="52f95-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52f95-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f95-125">CommonParameters</span></span>
<span data-ttu-id="52f95-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52f95-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f95-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52f95-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f95-128">輸入</span><span class="sxs-lookup"><span data-stu-id="52f95-128">INPUTS</span></span>

## <span data-ttu-id="52f95-129">輸出</span><span class="sxs-lookup"><span data-stu-id="52f95-129">OUTPUTS</span></span>

## <span data-ttu-id="52f95-130">筆記</span><span class="sxs-lookup"><span data-stu-id="52f95-130">NOTES</span></span>

## <span data-ttu-id="52f95-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="52f95-131">RELATED LINKS</span></span>

