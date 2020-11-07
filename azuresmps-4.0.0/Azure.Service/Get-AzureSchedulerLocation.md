---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967057"
---
# <span data-ttu-id="d45b5-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="d45b5-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="d45b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d45b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d45b5-103">取得可用的排程程式位置。</span><span class="sxs-lookup"><span data-stu-id="d45b5-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="d45b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d45b5-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d45b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d45b5-105">DESCRIPTION</span></span>
<span data-ttu-id="d45b5-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d45b5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d45b5-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="d45b5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d45b5-108">**AzureSchedulerLocation** Cmdlet 會取得可用的排程程式位置。</span><span class="sxs-lookup"><span data-stu-id="d45b5-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="d45b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="d45b5-109">EXAMPLES</span></span>

### <span data-ttu-id="d45b5-110">範例1：取得可用的排程程式位置</span><span class="sxs-lookup"><span data-stu-id="d45b5-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="d45b5-111">這個命令會取得可用的排程程式位置。</span><span class="sxs-lookup"><span data-stu-id="d45b5-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="d45b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="d45b5-112">PARAMETERS</span></span>

### <span data-ttu-id="d45b5-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d45b5-113">-Profile</span></span>
<span data-ttu-id="d45b5-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d45b5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d45b5-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d45b5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d45b5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45b5-116">CommonParameters</span></span>
<span data-ttu-id="d45b5-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d45b5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45b5-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d45b5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45b5-119">輸入</span><span class="sxs-lookup"><span data-stu-id="d45b5-119">INPUTS</span></span>

## <span data-ttu-id="d45b5-120">輸出</span><span class="sxs-lookup"><span data-stu-id="d45b5-120">OUTPUTS</span></span>

## <span data-ttu-id="d45b5-121">筆記</span><span class="sxs-lookup"><span data-stu-id="d45b5-121">NOTES</span></span>

## <span data-ttu-id="d45b5-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="d45b5-122">RELATED LINKS</span></span>

[<span data-ttu-id="d45b5-123">AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d45b5-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="d45b5-124">AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d45b5-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="d45b5-125">AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="d45b5-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


