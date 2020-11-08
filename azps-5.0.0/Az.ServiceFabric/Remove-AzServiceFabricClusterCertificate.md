---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137310"
---
# <span data-ttu-id="ca208-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ca208-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="ca208-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca208-102">SYNOPSIS</span></span>
<span data-ttu-id="ca208-103">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="ca208-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="ca208-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca208-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca208-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca208-105">DESCRIPTION</span></span>
<span data-ttu-id="ca208-106">使用 [ **移除-AzServiceFabricClusterCertificate** ] 從群集中移除群集憑證（只要已在群集中使用另一個有效的憑證）。</span><span class="sxs-lookup"><span data-stu-id="ca208-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="ca208-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca208-107">EXAMPLES</span></span>

### <span data-ttu-id="ca208-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ca208-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ca208-109">這個命令會移除具有指紋5F3660C715EBBDA31DB1FFDCF508302348DE8E7A 的憑證，以用於群集安全性。</span><span class="sxs-lookup"><span data-stu-id="ca208-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="ca208-110">參數</span><span class="sxs-lookup"><span data-stu-id="ca208-110">PARAMETERS</span></span>

### <span data-ttu-id="ca208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca208-111">-DefaultProfile</span></span>
<span data-ttu-id="ca208-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca208-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca208-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca208-113">-Name</span></span>
<span data-ttu-id="ca208-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca208-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ca208-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca208-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca208-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca208-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ca208-117">-指紋</span><span class="sxs-lookup"><span data-stu-id="ca208-117">-Thumbprint</span></span>
<span data-ttu-id="ca208-118">指定要移除的群集指紋。</span><span class="sxs-lookup"><span data-stu-id="ca208-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="ca208-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ca208-119">-Confirm</span></span>
<span data-ttu-id="ca208-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca208-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca208-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca208-121">-WhatIf</span></span>
<span data-ttu-id="ca208-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca208-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca208-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca208-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca208-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca208-124">CommonParameters</span></span>
<span data-ttu-id="ca208-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca208-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca208-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca208-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca208-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ca208-127">INPUTS</span></span>

### <span data-ttu-id="ca208-128">System.object</span><span class="sxs-lookup"><span data-stu-id="ca208-128">System.String</span></span>

## <span data-ttu-id="ca208-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ca208-129">OUTPUTS</span></span>

### <span data-ttu-id="ca208-130">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="ca208-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ca208-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ca208-131">NOTES</span></span>

## <span data-ttu-id="ca208-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca208-132">RELATED LINKS</span></span>
