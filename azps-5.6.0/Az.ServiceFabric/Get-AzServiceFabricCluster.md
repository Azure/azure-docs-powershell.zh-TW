---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902833"
---
# <span data-ttu-id="db376-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="db376-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="db376-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db376-102">SYNOPSIS</span></span>
<span data-ttu-id="db376-103">取得組群資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db376-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="db376-104">語法</span><span class="sxs-lookup"><span data-stu-id="db376-104">SYNTAX</span></span>

### <span data-ttu-id="db376-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="db376-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db376-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db376-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db376-107">ByName</span><span class="sxs-lookup"><span data-stu-id="db376-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db376-108">描述</span><span class="sxs-lookup"><span data-stu-id="db376-108">DESCRIPTION</span></span>
<span data-ttu-id="db376-109">**Get-AzServiceFabricCluster 會** 取得叢集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db376-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="db376-110">例子</span><span class="sxs-lookup"><span data-stu-id="db376-110">EXAMPLES</span></span>

### <span data-ttu-id="db376-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="db376-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="db376-112">此命令會取得叢集的叢集資源詳細資料，例如"myCluster"。</span><span class="sxs-lookup"><span data-stu-id="db376-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="db376-113">參數</span><span class="sxs-lookup"><span data-stu-id="db376-113">PARAMETERS</span></span>

### <span data-ttu-id="db376-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db376-114">-DefaultProfile</span></span>
<span data-ttu-id="db376-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db376-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db376-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="db376-116">-Name</span></span>
<span data-ttu-id="db376-117">指定組名</span><span class="sxs-lookup"><span data-stu-id="db376-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db376-118">-ResourceGroupName</span></span>
<span data-ttu-id="db376-119">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db376-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db376-120">CommonParameters</span></span>
<span data-ttu-id="db376-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db376-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db376-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db376-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db376-123">輸入</span><span class="sxs-lookup"><span data-stu-id="db376-123">INPUTS</span></span>

### <span data-ttu-id="db376-124">System.String</span><span class="sxs-lookup"><span data-stu-id="db376-124">System.String</span></span>

## <span data-ttu-id="db376-125">輸出</span><span class="sxs-lookup"><span data-stu-id="db376-125">OUTPUTS</span></span>

### <span data-ttu-id="db376-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="db376-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="db376-127">筆記</span><span class="sxs-lookup"><span data-stu-id="db376-127">NOTES</span></span>

## <span data-ttu-id="db376-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="db376-128">RELATED LINKS</span></span>
