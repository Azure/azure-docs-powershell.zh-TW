---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 0ef59a8071438fa1bfd1560ab2f2102722aa335f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447973"
---
# <span data-ttu-id="06ae8-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="06ae8-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="06ae8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="06ae8-103">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="06ae8-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06ae8-104">句法</span><span class="sxs-lookup"><span data-stu-id="06ae8-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06ae8-105">說明</span><span class="sxs-lookup"><span data-stu-id="06ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="06ae8-106">使用 [ **移除-AzureRmServiceFabricClusterCertificate** ] 從群集中移除群集憑證（只要已在群集中使用另一個有效的憑證）。</span><span class="sxs-lookup"><span data-stu-id="06ae8-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="06ae8-107">示例</span><span class="sxs-lookup"><span data-stu-id="06ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="06ae8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="06ae8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="06ae8-109">這個命令會移除具有指紋5F3660C715EBBDA31DB1FFDCF508302348DE8E7A 的憑證，以用於群集安全性。</span><span class="sxs-lookup"><span data-stu-id="06ae8-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="06ae8-110">參數</span><span class="sxs-lookup"><span data-stu-id="06ae8-110">PARAMETERS</span></span>

### <span data-ttu-id="06ae8-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="06ae8-111">-Name</span></span>
<span data-ttu-id="06ae8-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="06ae8-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ae8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ae8-113">-ResourceGroupName</span></span>
<span data-ttu-id="06ae8-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06ae8-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ae8-115">-指紋</span><span class="sxs-lookup"><span data-stu-id="06ae8-115">-Thumbprint</span></span>
<span data-ttu-id="06ae8-116">指定要移除的群集指紋。</span><span class="sxs-lookup"><span data-stu-id="06ae8-116">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ae8-117">-確認</span><span class="sxs-lookup"><span data-stu-id="06ae8-117">-Confirm</span></span>
<span data-ttu-id="06ae8-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06ae8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ae8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ae8-119">-WhatIf</span></span>
<span data-ttu-id="06ae8-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06ae8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06ae8-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06ae8-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ae8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ae8-122">-DefaultProfile</span></span>
<span data-ttu-id="06ae8-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06ae8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ae8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ae8-124">CommonParameters</span></span>
<span data-ttu-id="06ae8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06ae8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ae8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06ae8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ae8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="06ae8-127">INPUTS</span></span>

### <span data-ttu-id="06ae8-128">System.object</span><span class="sxs-lookup"><span data-stu-id="06ae8-128">System.String</span></span>

## <span data-ttu-id="06ae8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="06ae8-129">OUTPUTS</span></span>

### <span data-ttu-id="06ae8-130">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="06ae8-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="06ae8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="06ae8-131">NOTES</span></span>

## <span data-ttu-id="06ae8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="06ae8-132">RELATED LINKS</span></span>

