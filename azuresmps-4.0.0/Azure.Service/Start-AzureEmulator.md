---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967477"
---
# <span data-ttu-id="0c1c5-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="0c1c5-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="0c1c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1c5-103">啟動計算和儲存模擬程式。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="0c1c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c1c5-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c1c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c1c5-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0c1c5-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0c1c5-108">**AzureEmulator** Cmdlet 會啟動 compute 和 storage 模擬器，並在計算模擬器中託管目前的服務。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="0c1c5-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c1c5-109">EXAMPLES</span></span>

### <span data-ttu-id="0c1c5-110">範例1：啟動模擬器並啟動瀏覽器</span><span class="sxs-lookup"><span data-stu-id="0c1c5-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="0c1c5-111">這個範例會在 Azure 模擬器中執行服務，並在模擬服務上啟動新的瀏覽器視窗。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="0c1c5-112">參數</span><span class="sxs-lookup"><span data-stu-id="0c1c5-112">PARAMETERS</span></span>

### <span data-ttu-id="0c1c5-113">-啟動</span><span class="sxs-lookup"><span data-stu-id="0c1c5-113">-Launch</span></span>
<span data-ttu-id="0c1c5-114">將新的瀏覽器視窗託管在模擬器中後，就會在服務上開啟。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1c5-115">模式</span><span class="sxs-lookup"><span data-stu-id="0c1c5-115">-Mode</span></span>
<span data-ttu-id="0c1c5-116">指定模擬器模式。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="0c1c5-117">有效值為： Full 和 Express。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="0c1c5-118">預設值為 [Express]。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1c5-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0c1c5-119">-Profile</span></span>
<span data-ttu-id="0c1c5-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c1c5-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c1c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1c5-122">CommonParameters</span></span>
<span data-ttu-id="0c1c5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1c5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c1c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1c5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0c1c5-125">INPUTS</span></span>

## <span data-ttu-id="0c1c5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0c1c5-126">OUTPUTS</span></span>

## <span data-ttu-id="0c1c5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0c1c5-127">NOTES</span></span>

## <span data-ttu-id="0c1c5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c1c5-128">RELATED LINKS</span></span>

[<span data-ttu-id="0c1c5-129">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="0c1c5-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="0c1c5-130">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="0c1c5-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="0c1c5-131">停止 AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="0c1c5-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


