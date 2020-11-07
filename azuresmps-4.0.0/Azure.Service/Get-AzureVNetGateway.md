---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967725"
---
# <span data-ttu-id="2a807-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2a807-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="2a807-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a807-102">SYNOPSIS</span></span>
<span data-ttu-id="2a807-103">取得虛擬網路閘道的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a807-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="2a807-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a807-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2a807-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a807-105">DESCRIPTION</span></span>
<span data-ttu-id="2a807-106">**AzureVNetGateway** Cmdlet 會取得現有虛擬網路閘道的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a807-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="2a807-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a807-107">EXAMPLES</span></span>

### <span data-ttu-id="2a807-108">範例1：取得虛擬網路閘道的狀態</span><span class="sxs-lookup"><span data-stu-id="2a807-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="2a807-109">這個命令會取得虛擬網路閘道（名為 ContosoVN07 的虛擬網路閘道）的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a807-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="2a807-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a807-110">PARAMETERS</span></span>

### <span data-ttu-id="2a807-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2a807-111">-Profile</span></span>
<span data-ttu-id="2a807-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a807-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2a807-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2a807-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a807-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2a807-114">-VNetName</span></span>
<span data-ttu-id="2a807-115">指定包含此 Cmdlet 取得狀態之虛擬網路閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2a807-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="2a807-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a807-116">CommonParameters</span></span>
<span data-ttu-id="2a807-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a807-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a807-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a807-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a807-119">輸入</span><span class="sxs-lookup"><span data-stu-id="2a807-119">INPUTS</span></span>

## <span data-ttu-id="2a807-120">輸出</span><span class="sxs-lookup"><span data-stu-id="2a807-120">OUTPUTS</span></span>

## <span data-ttu-id="2a807-121">筆記</span><span class="sxs-lookup"><span data-stu-id="2a807-121">NOTES</span></span>

## <span data-ttu-id="2a807-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a807-122">RELATED LINKS</span></span>

[<span data-ttu-id="2a807-123">新-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2a807-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="2a807-124">移除-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2a807-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="2a807-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2a807-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="2a807-126">調整大小-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2a807-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="2a807-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="2a807-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


