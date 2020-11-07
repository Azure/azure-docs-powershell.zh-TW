---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968852"
---
# <span data-ttu-id="89f01-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89f01-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="89f01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89f01-102">SYNOPSIS</span></span>
<span data-ttu-id="89f01-103">移除虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="89f01-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="89f01-104">句法</span><span class="sxs-lookup"><span data-stu-id="89f01-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89f01-105">說明</span><span class="sxs-lookup"><span data-stu-id="89f01-105">DESCRIPTION</span></span>
<span data-ttu-id="89f01-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="89f01-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="89f01-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89f01-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="89f01-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="89f01-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="89f01-109">**WAPackVNet** Cmdlet 會移除虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="89f01-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="89f01-110">示例</span><span class="sxs-lookup"><span data-stu-id="89f01-110">EXAMPLES</span></span>

### <span data-ttu-id="89f01-111">範例1：移除虛擬化的網路</span><span class="sxs-lookup"><span data-stu-id="89f01-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="89f01-112">第一個命令會使用 **WAPackVNet** Cmdlet 取得名為 ContosoVNet01 的虛擬化網路，然後將該物件儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="89f01-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="89f01-113">第二個命令會移除儲存在 $VNet 中的虛擬化網路。</span><span class="sxs-lookup"><span data-stu-id="89f01-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="89f01-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89f01-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="89f01-115">範例2：移除虛擬化網路但不需確認</span><span class="sxs-lookup"><span data-stu-id="89f01-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="89f01-116">第一個命令會使用 **WAPackVNet** Cmdlet 取得名為 ContosoVNet02 的雲端服務，然後將該物件儲存在 $VNet 變數中。</span><span class="sxs-lookup"><span data-stu-id="89f01-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="89f01-117">第二個命令會移除儲存在 $VNet 中的虛擬化網路。</span><span class="sxs-lookup"><span data-stu-id="89f01-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="89f01-118">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="89f01-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="89f01-119">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89f01-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="89f01-120">參數</span><span class="sxs-lookup"><span data-stu-id="89f01-120">PARAMETERS</span></span>

### <span data-ttu-id="89f01-121">-Force</span><span class="sxs-lookup"><span data-stu-id="89f01-121">-Force</span></span>
<span data-ttu-id="89f01-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="89f01-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89f01-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89f01-123">-PassThru</span></span>
<span data-ttu-id="89f01-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="89f01-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89f01-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="89f01-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89f01-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="89f01-126">-Profile</span></span>
<span data-ttu-id="89f01-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="89f01-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89f01-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="89f01-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89f01-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="89f01-129">-VNet</span></span>
<span data-ttu-id="89f01-130">指定虛擬化的網路。</span><span class="sxs-lookup"><span data-stu-id="89f01-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="89f01-131">若要取得虛擬化的網路，請使用 **WAPackVNet** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89f01-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89f01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f01-132">CommonParameters</span></span>
<span data-ttu-id="89f01-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89f01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f01-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89f01-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f01-135">輸入</span><span class="sxs-lookup"><span data-stu-id="89f01-135">INPUTS</span></span>

## <span data-ttu-id="89f01-136">輸出</span><span class="sxs-lookup"><span data-stu-id="89f01-136">OUTPUTS</span></span>

## <span data-ttu-id="89f01-137">筆記</span><span class="sxs-lookup"><span data-stu-id="89f01-137">NOTES</span></span>

## <span data-ttu-id="89f01-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="89f01-138">RELATED LINKS</span></span>

[<span data-ttu-id="89f01-139">WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89f01-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="89f01-140">新-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89f01-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


