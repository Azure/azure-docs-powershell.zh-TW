---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 59f8723470707a644e426bd9559a8e982f731e6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915834"
---
# <span data-ttu-id="7dd69-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7dd69-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="7dd69-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7dd69-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd69-103">移除用於保護集區安全性的集區憑證。</span><span class="sxs-lookup"><span data-stu-id="7dd69-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="7dd69-104">語法</span><span class="sxs-lookup"><span data-stu-id="7dd69-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd69-105">描述</span><span class="sxs-lookup"><span data-stu-id="7dd69-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd69-106">使用 **Remove-AzServiceFabricClusterCertificate** 從叢集移除叢集憑證，只要該叢集中已有另一個有效憑證。</span><span class="sxs-lookup"><span data-stu-id="7dd69-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="7dd69-107">例子</span><span class="sxs-lookup"><span data-stu-id="7dd69-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd69-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7dd69-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="7dd69-109">此命令會移除使用指紋 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A 的憑證，以用於集區安全性。</span><span class="sxs-lookup"><span data-stu-id="7dd69-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="7dd69-110">參數</span><span class="sxs-lookup"><span data-stu-id="7dd69-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd69-111">-DefaultProfile</span></span>
<span data-ttu-id="7dd69-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dd69-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd69-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dd69-113">-Name</span></span>
<span data-ttu-id="7dd69-114">指定組名。</span><span class="sxs-lookup"><span data-stu-id="7dd69-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7dd69-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd69-115">-ResourceGroupName</span></span>
<span data-ttu-id="7dd69-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dd69-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7dd69-117">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="7dd69-117">-Thumbprint</span></span>
<span data-ttu-id="7dd69-118">指定要移除的圖樣集。</span><span class="sxs-lookup"><span data-stu-id="7dd69-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="7dd69-119">-確認</span><span class="sxs-lookup"><span data-stu-id="7dd69-119">-Confirm</span></span>
<span data-ttu-id="7dd69-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7dd69-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd69-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd69-121">-WhatIf</span></span>
<span data-ttu-id="7dd69-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7dd69-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dd69-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dd69-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd69-124">CommonParameters</span></span>
<span data-ttu-id="7dd69-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7dd69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd69-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dd69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd69-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7dd69-127">INPUTS</span></span>

### <span data-ttu-id="7dd69-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7dd69-128">System.String</span></span>

## <span data-ttu-id="7dd69-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7dd69-129">OUTPUTS</span></span>

### <span data-ttu-id="7dd69-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="7dd69-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7dd69-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7dd69-131">NOTES</span></span>

## <span data-ttu-id="7dd69-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dd69-132">RELATED LINKS</span></span>
