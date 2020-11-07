---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968016"
---
# <span data-ttu-id="b7867-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b7867-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="b7867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7867-102">SYNOPSIS</span></span>
<span data-ttu-id="b7867-103">在 Azure 中檢索有關 Azure RemoteApp 虛擬網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="b7867-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="b7867-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7867-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7867-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7867-105">DESCRIPTION</span></span>
<span data-ttu-id="b7867-106">**AzureRemoteAppVNet** Cmdlet 會在 Microsoft Azure 中檢索有關 Azure RemoteApp 虛擬網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="b7867-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="b7867-107">這個 Cmdlet 會傳回包含指定虛擬網路相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="b7867-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="b7867-108">如果未指定虛擬網路，此 Cmdlet 會傳回目前訂閱中所有虛擬網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7867-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="b7867-109">示例</span><span class="sxs-lookup"><span data-stu-id="b7867-109">EXAMPLES</span></span>

### <span data-ttu-id="b7867-110">範例1：檢索虛擬網路的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b7867-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="b7867-111">這個命令會取得名為 ContosoVNet 的虛擬網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7867-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="b7867-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7867-112">PARAMETERS</span></span>

### <span data-ttu-id="b7867-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="b7867-113">-IncludeSharedKey</span></span>
<span data-ttu-id="b7867-114">表示此 Cmdlet 在針對虛擬網路所取得的資訊中包含共用金鑰值。</span><span class="sxs-lookup"><span data-stu-id="b7867-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

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

### <span data-ttu-id="b7867-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b7867-115">-Profile</span></span>
<span data-ttu-id="b7867-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7867-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7867-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b7867-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7867-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b7867-118">-VNetName</span></span>
<span data-ttu-id="b7867-119">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7867-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="b7867-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7867-120">CommonParameters</span></span>
<span data-ttu-id="b7867-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7867-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7867-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7867-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7867-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b7867-123">INPUTS</span></span>

## <span data-ttu-id="b7867-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b7867-124">OUTPUTS</span></span>

## <span data-ttu-id="b7867-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b7867-125">NOTES</span></span>

## <span data-ttu-id="b7867-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7867-126">RELATED LINKS</span></span>

[<span data-ttu-id="b7867-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b7867-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


