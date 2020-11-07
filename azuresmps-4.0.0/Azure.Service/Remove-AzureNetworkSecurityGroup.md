---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967600"
---
# <span data-ttu-id="6e78d-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e78d-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="6e78d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e78d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e78d-103">刪除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="6e78d-103">Deletes a network security group.</span></span>

## <span data-ttu-id="6e78d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e78d-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e78d-105">說明</span><span class="sxs-lookup"><span data-stu-id="6e78d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e78d-106">**AzureNetworkSecurityGroup** Cmdlet 會從您的訂閱中刪除 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="6e78d-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="6e78d-107">示例</span><span class="sxs-lookup"><span data-stu-id="6e78d-107">EXAMPLES</span></span>

## <span data-ttu-id="6e78d-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e78d-108">PARAMETERS</span></span>

### <span data-ttu-id="6e78d-109">-Force</span><span class="sxs-lookup"><span data-stu-id="6e78d-109">-Force</span></span>
<span data-ttu-id="6e78d-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6e78d-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e78d-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e78d-111">-Name</span></span>
<span data-ttu-id="6e78d-112">指定此 Cmdlet 刪除之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e78d-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e78d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e78d-113">-PassThru</span></span>
<span data-ttu-id="6e78d-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6e78d-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6e78d-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6e78d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e78d-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6e78d-116">-Profile</span></span>
<span data-ttu-id="6e78d-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6e78d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6e78d-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6e78d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e78d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e78d-119">CommonParameters</span></span>
<span data-ttu-id="6e78d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e78d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e78d-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e78d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e78d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6e78d-122">INPUTS</span></span>

## <span data-ttu-id="6e78d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6e78d-123">OUTPUTS</span></span>

## <span data-ttu-id="6e78d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6e78d-124">NOTES</span></span>

## <span data-ttu-id="6e78d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e78d-125">RELATED LINKS</span></span>

[<span data-ttu-id="6e78d-126">AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e78d-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="6e78d-127">新-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e78d-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


