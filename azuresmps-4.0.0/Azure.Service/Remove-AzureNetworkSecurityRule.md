---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967315"
---
# <span data-ttu-id="11bd0-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="11bd0-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="11bd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="11bd0-103">從網路安全性群組移除網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="11bd0-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="11bd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="11bd0-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11bd0-105">說明</span><span class="sxs-lookup"><span data-stu-id="11bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="11bd0-106">**AzureNetworkSecurityRule** Cmdlet 會從網路安全性群組中移除 Azure 網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="11bd0-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="11bd0-107">示例</span><span class="sxs-lookup"><span data-stu-id="11bd0-107">EXAMPLES</span></span>

## <span data-ttu-id="11bd0-108">參數</span><span class="sxs-lookup"><span data-stu-id="11bd0-108">PARAMETERS</span></span>

### <span data-ttu-id="11bd0-109">-Force</span><span class="sxs-lookup"><span data-stu-id="11bd0-109">-Force</span></span>
<span data-ttu-id="11bd0-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="11bd0-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11bd0-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="11bd0-111">-Name</span></span>
<span data-ttu-id="11bd0-112">指定此 Cmdlet 移除之網路安全規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="11bd0-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="11bd0-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11bd0-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="11bd0-114">指定此 Cmdlet 修改的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="11bd0-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="11bd0-115">若要取得 **INetworkSecurityGroup** 物件，請使用 Get-AzureNetworkSecurityGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11bd0-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11bd0-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="11bd0-116">-Profile</span></span>
<span data-ttu-id="11bd0-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="11bd0-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="11bd0-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="11bd0-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11bd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bd0-119">CommonParameters</span></span>
<span data-ttu-id="11bd0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11bd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bd0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11bd0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bd0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="11bd0-122">INPUTS</span></span>

## <span data-ttu-id="11bd0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="11bd0-123">OUTPUTS</span></span>

## <span data-ttu-id="11bd0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="11bd0-124">NOTES</span></span>

## <span data-ttu-id="11bd0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="11bd0-125">RELATED LINKS</span></span>

[<span data-ttu-id="11bd0-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="11bd0-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


