---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967780"
---
# <span data-ttu-id="0c075-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c075-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="0c075-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c075-102">SYNOPSIS</span></span>
<span data-ttu-id="0c075-103">取得網路安全性群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c075-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="0c075-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c075-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c075-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c075-105">DESCRIPTION</span></span>
<span data-ttu-id="0c075-106">**AzureNetworkSecurityGroup** Cmdlet 會傳回 Azure 網路安全群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c075-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="0c075-107">指定 *詳細* 的參數以顯示網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="0c075-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="0c075-108">示例</span><span class="sxs-lookup"><span data-stu-id="0c075-108">EXAMPLES</span></span>

## <span data-ttu-id="0c075-109">參數</span><span class="sxs-lookup"><span data-stu-id="0c075-109">PARAMETERS</span></span>

### <span data-ttu-id="0c075-110">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="0c075-110">-Detailed</span></span>
<span data-ttu-id="0c075-111">表示此 Cmdlet 會傳回網路安全性群組的網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="0c075-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="0c075-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c075-112">-Name</span></span>
<span data-ttu-id="0c075-113">指定此 Cmdlet 所取得之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c075-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="0c075-114">在使用 Azure 入口網站 ***以外的資源*** 群組建立傳統網路安全性群組時，您必須使用下列 PowerShell 語法： `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` 。</span><span class="sxs-lookup"><span data-stu-id="0c075-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

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

### <span data-ttu-id="0c075-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0c075-115">-Profile</span></span>
<span data-ttu-id="0c075-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0c075-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c075-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0c075-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c075-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c075-118">CommonParameters</span></span>
<span data-ttu-id="0c075-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c075-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c075-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c075-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c075-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0c075-121">INPUTS</span></span>

## <span data-ttu-id="0c075-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0c075-122">OUTPUTS</span></span>

## <span data-ttu-id="0c075-123">筆記</span><span class="sxs-lookup"><span data-stu-id="0c075-123">NOTES</span></span>

## <span data-ttu-id="0c075-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c075-124">RELATED LINKS</span></span>

[<span data-ttu-id="0c075-125">新-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c075-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="0c075-126">移除-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c075-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

