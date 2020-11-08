---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967758"
---
# <span data-ttu-id="0ecb7-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="0ecb7-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="0ecb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ecb7-102">SYNOPSIS</span></span>
<span data-ttu-id="0ecb7-103">取得服務匯流排的位置。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="0ecb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ecb7-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ecb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ecb7-105">DESCRIPTION</span></span>
<span data-ttu-id="0ecb7-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0ecb7-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0ecb7-108">**AzureSBLocation** Cmdlet 會傳回服務匯流排可用的位置。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="0ecb7-109">示例</span><span class="sxs-lookup"><span data-stu-id="0ecb7-109">EXAMPLES</span></span>

### <span data-ttu-id="0ecb7-110">範例1：取得服務匯流排位置</span><span class="sxs-lookup"><span data-stu-id="0ecb7-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="0ecb7-111">這個範例會取得服務匯流排的位置。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="0ecb7-112">參數</span><span class="sxs-lookup"><span data-stu-id="0ecb7-112">PARAMETERS</span></span>

### <span data-ttu-id="0ecb7-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0ecb7-113">-Profile</span></span>
<span data-ttu-id="0ecb7-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ecb7-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ecb7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ecb7-116">CommonParameters</span></span>
<span data-ttu-id="0ecb7-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ecb7-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ecb7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ecb7-119">輸入</span><span class="sxs-lookup"><span data-stu-id="0ecb7-119">INPUTS</span></span>

## <span data-ttu-id="0ecb7-120">輸出</span><span class="sxs-lookup"><span data-stu-id="0ecb7-120">OUTPUTS</span></span>

## <span data-ttu-id="0ecb7-121">筆記</span><span class="sxs-lookup"><span data-stu-id="0ecb7-121">NOTES</span></span>

## <span data-ttu-id="0ecb7-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ecb7-122">RELATED LINKS</span></span>

[<span data-ttu-id="0ecb7-123">AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="0ecb7-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)

