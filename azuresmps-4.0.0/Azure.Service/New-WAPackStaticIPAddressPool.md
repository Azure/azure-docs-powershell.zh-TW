---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968827"
---
# <span data-ttu-id="40b45-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="40b45-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="40b45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40b45-102">SYNOPSIS</span></span>
<span data-ttu-id="40b45-103">建立靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="40b45-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="40b45-104">句法</span><span class="sxs-lookup"><span data-stu-id="40b45-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40b45-105">說明</span><span class="sxs-lookup"><span data-stu-id="40b45-105">DESCRIPTION</span></span>
<span data-ttu-id="40b45-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="40b45-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="40b45-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40b45-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="40b45-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="40b45-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="40b45-109">**新的-WAPackStaticIPAddressPool** Cmdlet 會建立靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="40b45-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="40b45-110">示例</span><span class="sxs-lookup"><span data-stu-id="40b45-110">EXAMPLES</span></span>

### <span data-ttu-id="40b45-111">範例1：建立靜態 IP 位址池</span><span class="sxs-lookup"><span data-stu-id="40b45-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="40b45-112">第一個命令首先會檢索要新增靜態 IP 位址池的虛擬機器網路。</span><span class="sxs-lookup"><span data-stu-id="40b45-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="40b45-113">此虛擬機器網路稱為 [ContosoVNet01]。</span><span class="sxs-lookup"><span data-stu-id="40b45-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="40b45-114">第二個命令使用先前檢索的虛擬機器網路來取得名為 ContosoVMSubnet01 的虛擬電腦子網，我們想要新增靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="40b45-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="40b45-115">最後一個命令會建立新的靜態 IP 位址池，其名稱為 ContosoStaticIpAddressPool01 且範圍開始192.168.1.0 與範圍結束192.168.1.10。</span><span class="sxs-lookup"><span data-stu-id="40b45-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="40b45-116">參數</span><span class="sxs-lookup"><span data-stu-id="40b45-116">PARAMETERS</span></span>

### <span data-ttu-id="40b45-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="40b45-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="40b45-118">指定靜態 IP 位址池的 IP 位址範圍結束時間。</span><span class="sxs-lookup"><span data-stu-id="40b45-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b45-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="40b45-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="40b45-120">指定靜態 IP 位址池的 IP 位址範圍起始。</span><span class="sxs-lookup"><span data-stu-id="40b45-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b45-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="40b45-121">-Name</span></span>
<span data-ttu-id="40b45-122">指定靜態 IP 位址池的名稱。</span><span class="sxs-lookup"><span data-stu-id="40b45-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b45-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="40b45-123">-Profile</span></span>
<span data-ttu-id="40b45-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="40b45-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40b45-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="40b45-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40b45-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="40b45-126">-VMSubnet</span></span>
<span data-ttu-id="40b45-127">指定與靜態 IP 位址池相關聯的 VMSubnet。</span><span class="sxs-lookup"><span data-stu-id="40b45-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="40b45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b45-128">CommonParameters</span></span>
<span data-ttu-id="40b45-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40b45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b45-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40b45-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b45-131">輸入</span><span class="sxs-lookup"><span data-stu-id="40b45-131">INPUTS</span></span>

## <span data-ttu-id="40b45-132">輸出</span><span class="sxs-lookup"><span data-stu-id="40b45-132">OUTPUTS</span></span>

## <span data-ttu-id="40b45-133">筆記</span><span class="sxs-lookup"><span data-stu-id="40b45-133">NOTES</span></span>

## <span data-ttu-id="40b45-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="40b45-134">RELATED LINKS</span></span>

[<span data-ttu-id="40b45-135">WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="40b45-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="40b45-136">移除-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="40b45-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


