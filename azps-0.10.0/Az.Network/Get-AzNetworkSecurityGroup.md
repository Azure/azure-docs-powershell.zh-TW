---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794403"
---
# <span data-ttu-id="49f8b-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49f8b-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="49f8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="49f8b-103">取得網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="49f8b-103">Gets a network security group.</span></span>

## <span data-ttu-id="49f8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="49f8b-104">SYNTAX</span></span>

### <span data-ttu-id="49f8b-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="49f8b-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49f8b-106">擴充</span><span class="sxs-lookup"><span data-stu-id="49f8b-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49f8b-107">說明</span><span class="sxs-lookup"><span data-stu-id="49f8b-107">DESCRIPTION</span></span>
<span data-ttu-id="49f8b-108">**AzNetworkSecurityGroup** Cmdlet 會取得 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="49f8b-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="49f8b-109">示例</span><span class="sxs-lookup"><span data-stu-id="49f8b-109">EXAMPLES</span></span>

### <span data-ttu-id="49f8b-110">1：檢索現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="49f8b-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="49f8b-111">這個命令會傳回資源群組 "rg1" 中的 Azure 網路安全性群組 "nsg1" 的內容</span><span class="sxs-lookup"><span data-stu-id="49f8b-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="49f8b-112">參數</span><span class="sxs-lookup"><span data-stu-id="49f8b-112">PARAMETERS</span></span>

### <span data-ttu-id="49f8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f8b-113">-DefaultProfile</span></span>
<span data-ttu-id="49f8b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49f8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f8b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="49f8b-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f8b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="49f8b-116">-Name</span></span>
<span data-ttu-id="49f8b-117">指定此 Cmdlet 所取得之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49f8b-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f8b-118">-ResourceGroupName</span></span>
<span data-ttu-id="49f8b-119">指定網路安全性群組所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49f8b-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f8b-120">CommonParameters</span></span>
<span data-ttu-id="49f8b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49f8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f8b-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49f8b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f8b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="49f8b-123">INPUTS</span></span>

## <span data-ttu-id="49f8b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="49f8b-124">OUTPUTS</span></span>

### <span data-ttu-id="49f8b-125">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49f8b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="49f8b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="49f8b-126">NOTES</span></span>

## <span data-ttu-id="49f8b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="49f8b-127">RELATED LINKS</span></span>

[<span data-ttu-id="49f8b-128">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49f8b-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="49f8b-129">移除-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49f8b-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="49f8b-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49f8b-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


