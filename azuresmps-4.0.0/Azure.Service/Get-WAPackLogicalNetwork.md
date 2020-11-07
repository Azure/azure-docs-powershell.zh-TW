---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968800"
---
# <span data-ttu-id="6a03e-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="6a03e-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="6a03e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a03e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a03e-103">取得邏輯網路物件。</span><span class="sxs-lookup"><span data-stu-id="6a03e-103">Gets logical network objects.</span></span>

## <span data-ttu-id="6a03e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a03e-104">SYNTAX</span></span>

### <span data-ttu-id="6a03e-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="6a03e-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6a03e-106">FromName</span><span class="sxs-lookup"><span data-stu-id="6a03e-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a03e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6a03e-107">DESCRIPTION</span></span>
<span data-ttu-id="6a03e-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="6a03e-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="6a03e-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a03e-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6a03e-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="6a03e-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6a03e-111">**WAPackLogicalNetwork** Cmdlet 會取得邏輯網路物件。</span><span class="sxs-lookup"><span data-stu-id="6a03e-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="6a03e-112">示例</span><span class="sxs-lookup"><span data-stu-id="6a03e-112">EXAMPLES</span></span>

### <span data-ttu-id="6a03e-113">範例1：使用名稱取得邏輯網路</span><span class="sxs-lookup"><span data-stu-id="6a03e-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="6a03e-114">這個命令會取得一個名為 ContosoLogicalNetwork01 的邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="6a03e-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="6a03e-115">範例2：取得所有邏輯網路</span><span class="sxs-lookup"><span data-stu-id="6a03e-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="6a03e-116">這個命令會取得所有邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="6a03e-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="6a03e-117">參數</span><span class="sxs-lookup"><span data-stu-id="6a03e-117">PARAMETERS</span></span>

### <span data-ttu-id="6a03e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a03e-118">-Name</span></span>
<span data-ttu-id="6a03e-119">指定邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a03e-119">Specifies the name of a logical network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a03e-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6a03e-120">-Profile</span></span>
<span data-ttu-id="6a03e-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6a03e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a03e-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6a03e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a03e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a03e-123">CommonParameters</span></span>
<span data-ttu-id="6a03e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a03e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a03e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a03e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a03e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6a03e-126">INPUTS</span></span>

## <span data-ttu-id="6a03e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6a03e-127">OUTPUTS</span></span>

## <span data-ttu-id="6a03e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6a03e-128">NOTES</span></span>

## <span data-ttu-id="6a03e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a03e-129">RELATED LINKS</span></span>

