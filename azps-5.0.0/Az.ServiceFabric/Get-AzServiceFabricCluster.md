---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138466"
---
# <span data-ttu-id="ab810-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab810-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="ab810-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab810-102">SYNOPSIS</span></span>
<span data-ttu-id="ab810-103">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab810-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="ab810-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab810-104">SYNTAX</span></span>

### <span data-ttu-id="ab810-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="ab810-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab810-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab810-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab810-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ab810-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab810-108">說明</span><span class="sxs-lookup"><span data-stu-id="ab810-108">DESCRIPTION</span></span>
<span data-ttu-id="ab810-109">**AzServiceFabricCluster** 將會取得群集資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab810-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="ab810-110">示例</span><span class="sxs-lookup"><span data-stu-id="ab810-110">EXAMPLES</span></span>

### <span data-ttu-id="ab810-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ab810-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="ab810-112">這個命令會取得群集 ' myCluster」的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab810-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="ab810-113">參數</span><span class="sxs-lookup"><span data-stu-id="ab810-113">PARAMETERS</span></span>

### <span data-ttu-id="ab810-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab810-114">-DefaultProfile</span></span>
<span data-ttu-id="ab810-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab810-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab810-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab810-116">-Name</span></span>
<span data-ttu-id="ab810-117">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="ab810-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ab810-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab810-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab810-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab810-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ab810-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab810-120">CommonParameters</span></span>
<span data-ttu-id="ab810-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab810-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab810-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab810-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab810-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ab810-123">INPUTS</span></span>

### <span data-ttu-id="ab810-124">System.object</span><span class="sxs-lookup"><span data-stu-id="ab810-124">System.String</span></span>

## <span data-ttu-id="ab810-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ab810-125">OUTPUTS</span></span>

### <span data-ttu-id="ab810-126">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="ab810-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ab810-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ab810-127">NOTES</span></span>

## <span data-ttu-id="ab810-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab810-128">RELATED LINKS</span></span>