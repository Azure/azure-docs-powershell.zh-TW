---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967356"
---
# <span data-ttu-id="08ccf-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="08ccf-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="08ccf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="08ccf-103">建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="08ccf-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="08ccf-104">句法</span><span class="sxs-lookup"><span data-stu-id="08ccf-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="08ccf-105">說明</span><span class="sxs-lookup"><span data-stu-id="08ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="08ccf-106">**新的-AzureNetworkSecurityGroup** Cmdlet 會在位置建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="08ccf-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="08ccf-107">示例</span><span class="sxs-lookup"><span data-stu-id="08ccf-107">EXAMPLES</span></span>

## <span data-ttu-id="08ccf-108">參數</span><span class="sxs-lookup"><span data-stu-id="08ccf-108">PARAMETERS</span></span>

### <span data-ttu-id="08ccf-109">-標籤</span><span class="sxs-lookup"><span data-stu-id="08ccf-109">-Label</span></span>
<span data-ttu-id="08ccf-110">指定新網路安全性群組的描述。</span><span class="sxs-lookup"><span data-stu-id="08ccf-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ccf-111">-位置</span><span class="sxs-lookup"><span data-stu-id="08ccf-111">-Location</span></span>
<span data-ttu-id="08ccf-112">指定此 Cmdlet 建立網路安全性群組的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="08ccf-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="08ccf-113">若要取得有效的位置，請使用 Get-AzureLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08ccf-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="08ccf-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="08ccf-114">-Name</span></span>
<span data-ttu-id="08ccf-115">指定新網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08ccf-115">Specifies a name for the new network security group.</span></span>

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

### <span data-ttu-id="08ccf-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="08ccf-116">-Profile</span></span>
<span data-ttu-id="08ccf-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="08ccf-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="08ccf-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="08ccf-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08ccf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ccf-119">CommonParameters</span></span>
<span data-ttu-id="08ccf-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08ccf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ccf-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08ccf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ccf-122">輸入</span><span class="sxs-lookup"><span data-stu-id="08ccf-122">INPUTS</span></span>

## <span data-ttu-id="08ccf-123">輸出</span><span class="sxs-lookup"><span data-stu-id="08ccf-123">OUTPUTS</span></span>

## <span data-ttu-id="08ccf-124">筆記</span><span class="sxs-lookup"><span data-stu-id="08ccf-124">NOTES</span></span>

## <span data-ttu-id="08ccf-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="08ccf-125">RELATED LINKS</span></span>

[<span data-ttu-id="08ccf-126">AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="08ccf-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


