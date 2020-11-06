---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 704c4c2a11cc83136481573190e745d7a4b2c83f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456519"
---
# <span data-ttu-id="7f47f-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f47f-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="7f47f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f47f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f47f-103">取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f47f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f47f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f47f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f47f-105">DESCRIPTION</span></span>
<span data-ttu-id="7f47f-106">**AzureRmApplicationSecurityGroup** Cmdlet 會取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="7f47f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f47f-107">EXAMPLES</span></span>

### <span data-ttu-id="7f47f-108">範例1：檢索所有應用程式的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="7f47f-109">上述命令會傳回訂閱中的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="7f47f-110">範例2：在資源群組中取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="7f47f-111">上述命令會傳回屬於資源群組 MyResourceGroup 的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7f47f-112">範例3：檢索特定的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="7f47f-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="7f47f-113">上述命令會傳回 [資源] 群組 MyResourceGroup 底下的 [應用程式安全性群組 MyApplicationSecurityGroup]。</span><span class="sxs-lookup"><span data-stu-id="7f47f-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="7f47f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f47f-114">PARAMETERS</span></span>

### <span data-ttu-id="7f47f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f47f-115">-DefaultProfile</span></span>
<span data-ttu-id="7f47f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f47f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f47f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f47f-117">-Name</span></span>
<span data-ttu-id="7f47f-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7f47f-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f47f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f47f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f47f-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f47f-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f47f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f47f-121">CommonParameters</span></span>
<span data-ttu-id="7f47f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f47f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f47f-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f47f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f47f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7f47f-124">INPUTS</span></span>

### <span data-ttu-id="7f47f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7f47f-125">System.String</span></span>

## <span data-ttu-id="7f47f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7f47f-126">OUTPUTS</span></span>

### <span data-ttu-id="7f47f-127">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7f47f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7f47f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7f47f-128">NOTES</span></span>

## <span data-ttu-id="7f47f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f47f-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f47f-130">新-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f47f-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7f47f-131">移除-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f47f-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7f47f-132">AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f47f-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f47f-133">AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f47f-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
