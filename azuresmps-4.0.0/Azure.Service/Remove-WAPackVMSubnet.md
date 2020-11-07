---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968853"
---
# <span data-ttu-id="85e05-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="85e05-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="85e05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85e05-102">SYNOPSIS</span></span>
<span data-ttu-id="85e05-103">移除虛擬電腦子網物件。</span><span class="sxs-lookup"><span data-stu-id="85e05-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="85e05-104">句法</span><span class="sxs-lookup"><span data-stu-id="85e05-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="85e05-105">說明</span><span class="sxs-lookup"><span data-stu-id="85e05-105">DESCRIPTION</span></span>
<span data-ttu-id="85e05-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="85e05-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="85e05-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85e05-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="85e05-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="85e05-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="85e05-109">**WAPackVMSubnet** Cmdlet 會移除虛擬機器子網物件。</span><span class="sxs-lookup"><span data-stu-id="85e05-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="85e05-110">示例</span><span class="sxs-lookup"><span data-stu-id="85e05-110">EXAMPLES</span></span>

### <span data-ttu-id="85e05-111">範例1：移除虛擬電腦子網</span><span class="sxs-lookup"><span data-stu-id="85e05-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="85e05-112">第一個命令會使用 **WAPackVMSubnet** Cmdlet 取得名為 ContosoVMSubnet01 的虛擬機器子網，然後將該物件儲存在 $VMSubnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e05-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="85e05-113">第二個命令會移除儲存在 $VMSubnet 中的虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="85e05-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="85e05-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85e05-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="85e05-115">範例2：不需確認即移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="85e05-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="85e05-116">第一個命令會使用 **WAPackVMSubnet** Cmdlet 取得名為 ContosoVMSubnet02 的雲端服務，然後將該物件儲存在 $VMSubnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e05-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="85e05-117">第二個命令會移除儲存在 $VMSubnet 中的虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="85e05-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="85e05-118">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="85e05-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="85e05-119">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85e05-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="85e05-120">參數</span><span class="sxs-lookup"><span data-stu-id="85e05-120">PARAMETERS</span></span>

### <span data-ttu-id="85e05-121">-Force</span><span class="sxs-lookup"><span data-stu-id="85e05-121">-Force</span></span>
<span data-ttu-id="85e05-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="85e05-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85e05-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85e05-123">-PassThru</span></span>
<span data-ttu-id="85e05-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="85e05-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85e05-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="85e05-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85e05-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="85e05-126">-Profile</span></span>
<span data-ttu-id="85e05-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="85e05-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85e05-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="85e05-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85e05-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="85e05-129">-VMSubnet</span></span>
<span data-ttu-id="85e05-130">指定虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="85e05-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="85e05-131">若要取得虛擬電腦子網，請使用 **WAPackVMSubnet** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85e05-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85e05-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e05-132">CommonParameters</span></span>
<span data-ttu-id="85e05-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85e05-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e05-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85e05-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e05-135">輸入</span><span class="sxs-lookup"><span data-stu-id="85e05-135">INPUTS</span></span>

## <span data-ttu-id="85e05-136">輸出</span><span class="sxs-lookup"><span data-stu-id="85e05-136">OUTPUTS</span></span>

## <span data-ttu-id="85e05-137">筆記</span><span class="sxs-lookup"><span data-stu-id="85e05-137">NOTES</span></span>

## <span data-ttu-id="85e05-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="85e05-138">RELATED LINKS</span></span>

[<span data-ttu-id="85e05-139">WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="85e05-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="85e05-140">新-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="85e05-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


