---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968801"
---
# <span data-ttu-id="5164f-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5164f-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="5164f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5164f-102">SYNOPSIS</span></span>
<span data-ttu-id="5164f-103">取得虛擬電腦子網物件。</span><span class="sxs-lookup"><span data-stu-id="5164f-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="5164f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5164f-104">SYNTAX</span></span>

### <span data-ttu-id="5164f-105">FromVMNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5164f-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5164f-106">FromName</span><span class="sxs-lookup"><span data-stu-id="5164f-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5164f-107">FromId</span><span class="sxs-lookup"><span data-stu-id="5164f-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5164f-108">說明</span><span class="sxs-lookup"><span data-stu-id="5164f-108">DESCRIPTION</span></span>
<span data-ttu-id="5164f-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="5164f-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5164f-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5164f-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5164f-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="5164f-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5164f-112">**WAPackVMSubnet** Cmdlet 會取得虛擬電腦子網物件。</span><span class="sxs-lookup"><span data-stu-id="5164f-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="5164f-113">示例</span><span class="sxs-lookup"><span data-stu-id="5164f-113">EXAMPLES</span></span>

### <span data-ttu-id="5164f-114">範例1：使用名稱取得虛擬機器子網</span><span class="sxs-lookup"><span data-stu-id="5164f-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="5164f-115">這個命令會取得名為 ContosoSubnet01 的虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="5164f-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="5164f-116">範例2：使用識別碼取得虛擬機器子網</span><span class="sxs-lookup"><span data-stu-id="5164f-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5164f-117">這個命令會取得具有指定識別碼的虛擬機器子網。</span><span class="sxs-lookup"><span data-stu-id="5164f-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="5164f-118">範例3：從指定的虛擬化網路取得所有虛擬機器子網</span><span class="sxs-lookup"><span data-stu-id="5164f-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="5164f-119">這個命令會從指定的虛擬化網路中取得所有的虛擬機器子網。</span><span class="sxs-lookup"><span data-stu-id="5164f-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="5164f-120">參數</span><span class="sxs-lookup"><span data-stu-id="5164f-120">PARAMETERS</span></span>

### <span data-ttu-id="5164f-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5164f-121">-ID</span></span>
<span data-ttu-id="5164f-122">指定虛擬電腦子網的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5164f-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5164f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5164f-123">-Name</span></span>
<span data-ttu-id="5164f-124">指定虛擬電腦子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="5164f-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5164f-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5164f-125">-Profile</span></span>
<span data-ttu-id="5164f-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5164f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5164f-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5164f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5164f-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="5164f-128">-VNet</span></span>
<span data-ttu-id="5164f-129">指定與虛擬電腦子網相關聯的 VNet。</span><span class="sxs-lookup"><span data-stu-id="5164f-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

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

### <span data-ttu-id="5164f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5164f-130">CommonParameters</span></span>
<span data-ttu-id="5164f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5164f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5164f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5164f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5164f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5164f-133">INPUTS</span></span>

## <span data-ttu-id="5164f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5164f-134">OUTPUTS</span></span>

## <span data-ttu-id="5164f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5164f-135">NOTES</span></span>

## <span data-ttu-id="5164f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5164f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5164f-137">WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="5164f-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="5164f-138">新-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5164f-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="5164f-139">移除-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5164f-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


