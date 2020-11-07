---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968843"
---
# <span data-ttu-id="ce306-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce306-101">New-WAPackVNet</span></span>

## <span data-ttu-id="ce306-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce306-102">SYNOPSIS</span></span>
<span data-ttu-id="ce306-103">建立虛擬化的網路。</span><span class="sxs-lookup"><span data-stu-id="ce306-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="ce306-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce306-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce306-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce306-105">DESCRIPTION</span></span>
<span data-ttu-id="ce306-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="ce306-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ce306-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce306-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ce306-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ce306-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ce306-109">**新的-WAPackVNet** Cmdlet 會建立虛擬化的網路。</span><span class="sxs-lookup"><span data-stu-id="ce306-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="ce306-110">示例</span><span class="sxs-lookup"><span data-stu-id="ce306-110">EXAMPLES</span></span>

### <span data-ttu-id="ce306-111">範例1：建立虛擬化的網路</span><span class="sxs-lookup"><span data-stu-id="ce306-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="ce306-112">第一個命令首先會檢索要新增新虛擬化網路的邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="ce306-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="ce306-113">這個邏輯網路名為 ContosoLogicalNetwork01。</span><span class="sxs-lookup"><span data-stu-id="ce306-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="ce306-114">第二個和 [上一個] 命令會使用先前檢索的邏輯網路建立虛擬化網路，名稱 (ContosoVNett01) ，以及 (描述) 描述。</span><span class="sxs-lookup"><span data-stu-id="ce306-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="ce306-115">參數</span><span class="sxs-lookup"><span data-stu-id="ce306-115">PARAMETERS</span></span>

### <span data-ttu-id="ce306-116">-描述</span><span class="sxs-lookup"><span data-stu-id="ce306-116">-Description</span></span>
<span data-ttu-id="ce306-117">指定虛擬化網路的描述。</span><span class="sxs-lookup"><span data-stu-id="ce306-117">Specifies a description for the virtualized network.</span></span>

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

### <span data-ttu-id="ce306-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="ce306-118">-LogicalNetwork</span></span>
<span data-ttu-id="ce306-119">指定與虛擬化網路相關聯的 LogicalNetwork。</span><span class="sxs-lookup"><span data-stu-id="ce306-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce306-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce306-120">-Name</span></span>
<span data-ttu-id="ce306-121">指定虛擬化網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce306-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="ce306-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ce306-122">-Profile</span></span>
<span data-ttu-id="ce306-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ce306-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce306-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ce306-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce306-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce306-125">CommonParameters</span></span>
<span data-ttu-id="ce306-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce306-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce306-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce306-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce306-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ce306-128">INPUTS</span></span>

## <span data-ttu-id="ce306-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ce306-129">OUTPUTS</span></span>

## <span data-ttu-id="ce306-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ce306-130">NOTES</span></span>

## <span data-ttu-id="ce306-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce306-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce306-132">WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce306-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="ce306-133">移除-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce306-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


