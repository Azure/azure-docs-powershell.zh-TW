---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968799"
---
# <span data-ttu-id="5ce2e-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5ce2e-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="5ce2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce2e-103">取得雲端服務物件。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="5ce2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce2e-104">SYNTAX</span></span>

### <span data-ttu-id="5ce2e-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="5ce2e-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5ce2e-106">FromName</span><span class="sxs-lookup"><span data-stu-id="5ce2e-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ce2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ce2e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce2e-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5ce2e-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5ce2e-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5ce2e-111">**WAPackCloudService** Cmdlet 會取得雲端服務物件。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="5ce2e-112">示例</span><span class="sxs-lookup"><span data-stu-id="5ce2e-112">EXAMPLES</span></span>

## <span data-ttu-id="5ce2e-113">參數</span><span class="sxs-lookup"><span data-stu-id="5ce2e-113">PARAMETERS</span></span>

### <span data-ttu-id="5ce2e-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ce2e-114">-Name</span></span>
<span data-ttu-id="5ce2e-115">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="5ce2e-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5ce2e-116">-Profile</span></span>
<span data-ttu-id="5ce2e-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ce2e-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ce2e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce2e-119">CommonParameters</span></span>
<span data-ttu-id="5ce2e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce2e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ce2e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce2e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce2e-122">INPUTS</span></span>

## <span data-ttu-id="5ce2e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce2e-123">OUTPUTS</span></span>

## <span data-ttu-id="5ce2e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce2e-124">NOTES</span></span>

## <span data-ttu-id="5ce2e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce2e-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ce2e-126">新-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5ce2e-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="5ce2e-127">移除-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="5ce2e-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


