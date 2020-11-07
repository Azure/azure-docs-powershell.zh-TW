---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968877"
---
# <span data-ttu-id="fb985-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fb985-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="fb985-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb985-102">SYNOPSIS</span></span>
<span data-ttu-id="fb985-103">取得靜態 IP 位址池物件。</span><span class="sxs-lookup"><span data-stu-id="fb985-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="fb985-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb985-104">SYNTAX</span></span>

### <span data-ttu-id="fb985-105">FromVMSubnetObject (預設) </span><span class="sxs-lookup"><span data-stu-id="fb985-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fb985-106">FromName</span><span class="sxs-lookup"><span data-stu-id="fb985-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb985-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb985-107">DESCRIPTION</span></span>
<span data-ttu-id="fb985-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="fb985-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="fb985-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb985-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fb985-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="fb985-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fb985-111">**WAPackStaticIPAddressPool** Cmdlet 會取得靜態 IP 位址池物件。</span><span class="sxs-lookup"><span data-stu-id="fb985-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="fb985-112">示例</span><span class="sxs-lookup"><span data-stu-id="fb985-112">EXAMPLES</span></span>

### <span data-ttu-id="fb985-113">範例1：從指定的 VMSubnet 取得靜態 IP 位址池</span><span class="sxs-lookup"><span data-stu-id="fb985-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="fb985-114">這個命令會從指定的 VMSubnet 取得名為 ContosoStaticIPAddressPool01 的靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="fb985-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="fb985-115">範例2：從指定的 VMSubnet 取得所有靜態 IP 位址池</span><span class="sxs-lookup"><span data-stu-id="fb985-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="fb985-116">這個命令會從指定的 VMSubet 取得所有靜態 IP 池。</span><span class="sxs-lookup"><span data-stu-id="fb985-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="fb985-117">參數</span><span class="sxs-lookup"><span data-stu-id="fb985-117">PARAMETERS</span></span>

### <span data-ttu-id="fb985-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb985-118">-Name</span></span>
<span data-ttu-id="fb985-119">指定靜態 IP 位址池的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb985-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="fb985-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fb985-120">-Profile</span></span>
<span data-ttu-id="fb985-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb985-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb985-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fb985-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb985-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="fb985-123">-VMSubnet</span></span>
<span data-ttu-id="fb985-124">指定與靜態 IP 位址池相關聯的 **VMSubnet** 物件。</span><span class="sxs-lookup"><span data-stu-id="fb985-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="fb985-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb985-125">CommonParameters</span></span>
<span data-ttu-id="fb985-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb985-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb985-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb985-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb985-128">輸入</span><span class="sxs-lookup"><span data-stu-id="fb985-128">INPUTS</span></span>

## <span data-ttu-id="fb985-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fb985-129">OUTPUTS</span></span>

## <span data-ttu-id="fb985-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fb985-130">NOTES</span></span>

## <span data-ttu-id="fb985-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb985-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb985-132">新-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fb985-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="fb985-133">移除-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fb985-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


