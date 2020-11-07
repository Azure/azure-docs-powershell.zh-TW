---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967779"
---
# <span data-ttu-id="518b3-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="518b3-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="518b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="518b3-102">SYNOPSIS</span></span>
<span data-ttu-id="518b3-103">取得網路安全性群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="518b3-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="518b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="518b3-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="518b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="518b3-105">DESCRIPTION</span></span>
<span data-ttu-id="518b3-106">**AzureNetworkSecurityGroupConfig** Cmdlet 會傳回網路安全性群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="518b3-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="518b3-107">指定 *詳細* 的參數以顯示網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="518b3-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="518b3-108">示例</span><span class="sxs-lookup"><span data-stu-id="518b3-108">EXAMPLES</span></span>

## <span data-ttu-id="518b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="518b3-109">PARAMETERS</span></span>

### <span data-ttu-id="518b3-110">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="518b3-110">-Detailed</span></span>
<span data-ttu-id="518b3-111">表示此 Cmdlet 會顯示網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="518b3-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="518b3-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="518b3-112">-Profile</span></span>
<span data-ttu-id="518b3-113">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="518b3-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="518b3-114">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="518b3-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="518b3-115">-VM</span><span class="sxs-lookup"><span data-stu-id="518b3-115">-VM</span></span>
<span data-ttu-id="518b3-116">指定此 Cmdlet 取得網路安全性群組詳細資料的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="518b3-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="518b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518b3-117">CommonParameters</span></span>
<span data-ttu-id="518b3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="518b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518b3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="518b3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518b3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="518b3-120">INPUTS</span></span>

## <span data-ttu-id="518b3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="518b3-121">OUTPUTS</span></span>

## <span data-ttu-id="518b3-122">筆記</span><span class="sxs-lookup"><span data-stu-id="518b3-122">NOTES</span></span>

## <span data-ttu-id="518b3-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="518b3-123">RELATED LINKS</span></span>

[<span data-ttu-id="518b3-124">新-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="518b3-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="518b3-125">移除-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="518b3-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


