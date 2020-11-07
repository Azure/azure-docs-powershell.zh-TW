---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967592"
---
# <span data-ttu-id="162a6-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="162a6-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="162a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="162a6-102">SYNOPSIS</span></span>
<span data-ttu-id="162a6-103">刪除 Azure RemoteApp 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="162a6-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="162a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="162a6-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="162a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="162a6-105">DESCRIPTION</span></span>
<span data-ttu-id="162a6-106">**AzureRemoteAppVNet** Cmdlet 會刪除 Azure RemoteApp 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="162a6-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="162a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="162a6-107">EXAMPLES</span></span>

### <span data-ttu-id="162a6-108">範例1：刪除指定的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="162a6-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="162a6-109">這個命令會刪除名為 ContosoVNet 的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="162a6-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="162a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="162a6-110">PARAMETERS</span></span>

### <span data-ttu-id="162a6-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="162a6-111">-Profile</span></span>
<span data-ttu-id="162a6-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="162a6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="162a6-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="162a6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="162a6-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="162a6-114">-VNetName</span></span>
<span data-ttu-id="162a6-115">指定要刪除之 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="162a6-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="162a6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162a6-116">CommonParameters</span></span>
<span data-ttu-id="162a6-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="162a6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162a6-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="162a6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162a6-119">輸入</span><span class="sxs-lookup"><span data-stu-id="162a6-119">INPUTS</span></span>

## <span data-ttu-id="162a6-120">輸出</span><span class="sxs-lookup"><span data-stu-id="162a6-120">OUTPUTS</span></span>

## <span data-ttu-id="162a6-121">筆記</span><span class="sxs-lookup"><span data-stu-id="162a6-121">NOTES</span></span>

## <span data-ttu-id="162a6-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="162a6-122">RELATED LINKS</span></span>

[<span data-ttu-id="162a6-123">AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="162a6-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="162a6-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="162a6-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


