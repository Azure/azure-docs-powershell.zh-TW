---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794445"
---
# <span data-ttu-id="fffc2-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fffc2-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="fffc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fffc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fffc2-103">取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-103">Gets an application security group.</span></span>

## <span data-ttu-id="fffc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fffc2-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fffc2-105">說明</span><span class="sxs-lookup"><span data-stu-id="fffc2-105">DESCRIPTION</span></span>
<span data-ttu-id="fffc2-106">**AzApplicationSecurityGroup** Cmdlet 會取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="fffc2-107">示例</span><span class="sxs-lookup"><span data-stu-id="fffc2-107">EXAMPLES</span></span>

### <span data-ttu-id="fffc2-108">範例1：檢索所有應用程式的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="fffc2-109">上述命令會傳回訂閱中的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="fffc2-110">範例2：在資源群組中取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="fffc2-111">上述命令會傳回屬於資源群組 MyResourceGroup 的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="fffc2-112">範例3：檢索特定的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fffc2-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="fffc2-113">上述命令會傳回 [資源] 群組 MyResourceGroup 底下的 [應用程式安全性群組 MyApplicationSecurityGroup]。</span><span class="sxs-lookup"><span data-stu-id="fffc2-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="fffc2-114">參數</span><span class="sxs-lookup"><span data-stu-id="fffc2-114">PARAMETERS</span></span>

### <span data-ttu-id="fffc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffc2-115">-DefaultProfile</span></span>
<span data-ttu-id="fffc2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fffc2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fffc2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fffc2-117">-Name</span></span>
<span data-ttu-id="fffc2-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fffc2-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fffc2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffc2-119">-ResourceGroupName</span></span>
<span data-ttu-id="fffc2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffc2-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fffc2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffc2-121">CommonParameters</span></span>
<span data-ttu-id="fffc2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fffc2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffc2-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fffc2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffc2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fffc2-124">INPUTS</span></span>

### <span data-ttu-id="fffc2-125">System.object</span><span class="sxs-lookup"><span data-stu-id="fffc2-125">System.String</span></span>

## <span data-ttu-id="fffc2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fffc2-126">OUTPUTS</span></span>

### <span data-ttu-id="fffc2-127">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fffc2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="fffc2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fffc2-128">NOTES</span></span>

## <span data-ttu-id="fffc2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fffc2-129">RELATED LINKS</span></span>

[<span data-ttu-id="fffc2-130">新-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fffc2-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="fffc2-131">移除-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fffc2-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="fffc2-132">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fffc2-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fffc2-133">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fffc2-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
