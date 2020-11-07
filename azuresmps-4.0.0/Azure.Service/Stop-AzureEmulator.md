---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd94462eb89cff6b4cec97f05911e27dbb05c920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967212"
---
# <span data-ttu-id="8f260-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="8f260-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="8f260-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f260-102">SYNOPSIS</span></span>
<span data-ttu-id="8f260-103">停止計算模擬器。</span><span class="sxs-lookup"><span data-stu-id="8f260-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="8f260-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f260-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f260-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f260-105">DESCRIPTION</span></span>
<span data-ttu-id="8f260-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f260-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8f260-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="8f260-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8f260-108">**AzureEmulator** Cmdlet 會停止 Azure 計算模擬器。</span><span class="sxs-lookup"><span data-stu-id="8f260-108">The **Stop-AzureEmulator** cmdlet stops the Azure compute emulator.</span></span>
<span data-ttu-id="8f260-109">任何目前在模擬器中執行的服務都會被移除。</span><span class="sxs-lookup"><span data-stu-id="8f260-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="8f260-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f260-110">EXAMPLES</span></span>

## <span data-ttu-id="8f260-111">參數</span><span class="sxs-lookup"><span data-stu-id="8f260-111">PARAMETERS</span></span>

### <span data-ttu-id="8f260-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f260-112">-PassThru</span></span>
<span data-ttu-id="8f260-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8f260-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f260-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8f260-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f260-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8f260-115">-Profile</span></span>
<span data-ttu-id="8f260-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f260-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f260-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8f260-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f260-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f260-118">CommonParameters</span></span>
<span data-ttu-id="8f260-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f260-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f260-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f260-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f260-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8f260-121">INPUTS</span></span>

## <span data-ttu-id="8f260-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8f260-122">OUTPUTS</span></span>

## <span data-ttu-id="8f260-123">筆記</span><span class="sxs-lookup"><span data-stu-id="8f260-123">NOTES</span></span>

## <span data-ttu-id="8f260-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f260-124">RELATED LINKS</span></span>

[<span data-ttu-id="8f260-125">開始-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="8f260-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


