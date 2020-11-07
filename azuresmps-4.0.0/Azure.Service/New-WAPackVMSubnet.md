---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967332"
---
# <span data-ttu-id="17119-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="17119-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="17119-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17119-102">SYNOPSIS</span></span>
<span data-ttu-id="17119-103">建立虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="17119-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="17119-104">句法</span><span class="sxs-lookup"><span data-stu-id="17119-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="17119-105">說明</span><span class="sxs-lookup"><span data-stu-id="17119-105">DESCRIPTION</span></span>
<span data-ttu-id="17119-106">**新的-WAPackVMSubnet** Cmdlet 會建立一個虛擬電腦子網。</span><span class="sxs-lookup"><span data-stu-id="17119-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="17119-107">示例</span><span class="sxs-lookup"><span data-stu-id="17119-107">EXAMPLES</span></span>

### <span data-ttu-id="17119-108">範例1：建立虛擬電腦子網</span><span class="sxs-lookup"><span data-stu-id="17119-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="17119-109">第一個命令首先會檢索要新增虛擬電腦子網的虛擬機器網路。</span><span class="sxs-lookup"><span data-stu-id="17119-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="17119-110">此虛擬機器網路稱為 [ContosoVNet01]。</span><span class="sxs-lookup"><span data-stu-id="17119-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="17119-111">第二個命令會使用先前取得的虛擬機器網路、名稱 ContosoVMSubnet01 及子網 192.168.1.0/24 來建立虛擬機器子網。</span><span class="sxs-lookup"><span data-stu-id="17119-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="17119-112">參數</span><span class="sxs-lookup"><span data-stu-id="17119-112">PARAMETERS</span></span>

### <span data-ttu-id="17119-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="17119-113">-Name</span></span>
<span data-ttu-id="17119-114">指定虛擬機器子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="17119-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="17119-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="17119-115">-Profile</span></span>
<span data-ttu-id="17119-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="17119-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17119-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="17119-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17119-118">-子網</span><span class="sxs-lookup"><span data-stu-id="17119-118">-Subnet</span></span>
<span data-ttu-id="17119-119">指定虛擬機器子網的子網。</span><span class="sxs-lookup"><span data-stu-id="17119-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="17119-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="17119-120">-VNet</span></span>
<span data-ttu-id="17119-121">指定與虛擬電腦子網相關聯的 VNet。</span><span class="sxs-lookup"><span data-stu-id="17119-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

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

### <span data-ttu-id="17119-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17119-122">CommonParameters</span></span>
<span data-ttu-id="17119-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17119-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17119-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17119-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17119-125">輸入</span><span class="sxs-lookup"><span data-stu-id="17119-125">INPUTS</span></span>

## <span data-ttu-id="17119-126">輸出</span><span class="sxs-lookup"><span data-stu-id="17119-126">OUTPUTS</span></span>

## <span data-ttu-id="17119-127">筆記</span><span class="sxs-lookup"><span data-stu-id="17119-127">NOTES</span></span>

## <span data-ttu-id="17119-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="17119-128">RELATED LINKS</span></span>

[<span data-ttu-id="17119-129">WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="17119-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="17119-130">WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="17119-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="17119-131">移除-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="17119-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


