---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452183"
---
# <span data-ttu-id="ca311-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca311-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="ca311-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca311-102">SYNOPSIS</span></span>
<span data-ttu-id="ca311-103">取得網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ca311-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca311-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca311-104">SYNTAX</span></span>

### <span data-ttu-id="ca311-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ca311-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca311-106">擴充</span><span class="sxs-lookup"><span data-stu-id="ca311-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca311-107">說明</span><span class="sxs-lookup"><span data-stu-id="ca311-107">DESCRIPTION</span></span>
<span data-ttu-id="ca311-108">**AzureRmNetworkSecurityGroup** Cmdlet 會取得 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ca311-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="ca311-109">示例</span><span class="sxs-lookup"><span data-stu-id="ca311-109">EXAMPLES</span></span>

### <span data-ttu-id="ca311-110">1：檢索現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="ca311-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="ca311-111">這個命令會傳回資源群組 "rg1" 中的 Azure 網路安全性群組 "nsg1" 的內容</span><span class="sxs-lookup"><span data-stu-id="ca311-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="ca311-112">參數</span><span class="sxs-lookup"><span data-stu-id="ca311-112">PARAMETERS</span></span>

### <span data-ttu-id="ca311-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca311-113">-DefaultProfile</span></span>
<span data-ttu-id="ca311-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca311-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca311-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ca311-115">-ExpandResource</span></span>
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

### <span data-ttu-id="ca311-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca311-116">-Name</span></span>
<span data-ttu-id="ca311-117">指定此 Cmdlet 所取得之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca311-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ca311-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca311-118">-ResourceGroupName</span></span>
<span data-ttu-id="ca311-119">指定網路安全性群組所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca311-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="ca311-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca311-120">CommonParameters</span></span>
<span data-ttu-id="ca311-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca311-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca311-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca311-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca311-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ca311-123">INPUTS</span></span>

### <span data-ttu-id="ca311-124">所有</span><span class="sxs-lookup"><span data-stu-id="ca311-124">None</span></span>
<span data-ttu-id="ca311-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ca311-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca311-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ca311-126">OUTPUTS</span></span>

### <span data-ttu-id="ca311-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca311-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ca311-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ca311-128">NOTES</span></span>

## <span data-ttu-id="ca311-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca311-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca311-130">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca311-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ca311-131">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca311-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ca311-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca311-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


