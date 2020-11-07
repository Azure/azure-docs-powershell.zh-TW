---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: e0a9bd49ca49ae4df1ae83d9c93a191f406c442a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799817"
---
# <span data-ttu-id="b8166-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8166-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="b8166-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8166-102">SYNOPSIS</span></span>
<span data-ttu-id="b8166-103">取得網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="b8166-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8166-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8166-104">SYNTAX</span></span>

### <span data-ttu-id="b8166-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="b8166-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8166-106">擴充</span><span class="sxs-lookup"><span data-stu-id="b8166-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8166-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8166-107">DESCRIPTION</span></span>
<span data-ttu-id="b8166-108">**AzureRmNetworkSecurityGroup** Cmdlet 會取得 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="b8166-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="b8166-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8166-109">EXAMPLES</span></span>

### <span data-ttu-id="b8166-110">1：檢索現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="b8166-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="b8166-111">這個命令會傳回資源群組 "rg1" 中的 Azure 網路安全性群組 "nsg1" 的內容</span><span class="sxs-lookup"><span data-stu-id="b8166-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="b8166-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8166-112">PARAMETERS</span></span>

### <span data-ttu-id="b8166-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8166-113">-DefaultProfile</span></span>
<span data-ttu-id="b8166-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8166-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8166-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b8166-115">-ExpandResource</span></span>
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

### <span data-ttu-id="b8166-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8166-116">-Name</span></span>
<span data-ttu-id="b8166-117">指定此 Cmdlet 所取得之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8166-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b8166-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8166-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8166-119">指定網路安全性群組所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8166-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="b8166-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8166-120">CommonParameters</span></span>
<span data-ttu-id="b8166-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8166-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8166-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8166-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8166-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b8166-123">INPUTS</span></span>

## <span data-ttu-id="b8166-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b8166-124">OUTPUTS</span></span>

### <span data-ttu-id="b8166-125">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8166-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b8166-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b8166-126">NOTES</span></span>

## <span data-ttu-id="b8166-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8166-127">RELATED LINKS</span></span>

[<span data-ttu-id="b8166-128">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8166-128">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="b8166-129">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8166-129">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="b8166-130">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8166-130">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


