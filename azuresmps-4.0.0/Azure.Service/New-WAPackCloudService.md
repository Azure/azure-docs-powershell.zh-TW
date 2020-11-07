---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968803"
---
# <span data-ttu-id="ee472-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ee472-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="ee472-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee472-102">SYNOPSIS</span></span>
<span data-ttu-id="ee472-103">建立雲端服務。</span><span class="sxs-lookup"><span data-stu-id="ee472-103">Creates a cloud service.</span></span>

## <span data-ttu-id="ee472-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee472-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee472-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee472-105">DESCRIPTION</span></span>
<span data-ttu-id="ee472-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="ee472-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ee472-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee472-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ee472-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ee472-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ee472-109">**新的-WAPackCloudService** Cmdlet 會建立雲端服務。</span><span class="sxs-lookup"><span data-stu-id="ee472-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="ee472-110">示例</span><span class="sxs-lookup"><span data-stu-id="ee472-110">EXAMPLES</span></span>

### <span data-ttu-id="ee472-111">範例1：建立雲端服務</span><span class="sxs-lookup"><span data-stu-id="ee472-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="ee472-112">此命令會建立一個名為 ContosoCloudService01 的雲端服務與標籤。</span><span class="sxs-lookup"><span data-stu-id="ee472-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="ee472-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee472-113">PARAMETERS</span></span>

### <span data-ttu-id="ee472-114">-標籤</span><span class="sxs-lookup"><span data-stu-id="ee472-114">-Label</span></span>
<span data-ttu-id="ee472-115">指定雲端服務的標籤。</span><span class="sxs-lookup"><span data-stu-id="ee472-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="ee472-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee472-116">-Name</span></span>
<span data-ttu-id="ee472-117">指定 cloudservice 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee472-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="ee472-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ee472-118">-Profile</span></span>
<span data-ttu-id="ee472-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ee472-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee472-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ee472-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee472-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee472-121">CommonParameters</span></span>
<span data-ttu-id="ee472-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee472-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee472-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee472-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee472-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ee472-124">INPUTS</span></span>

## <span data-ttu-id="ee472-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ee472-125">OUTPUTS</span></span>

## <span data-ttu-id="ee472-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ee472-126">NOTES</span></span>

## <span data-ttu-id="ee472-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee472-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee472-128">WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ee472-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="ee472-129">移除-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ee472-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


