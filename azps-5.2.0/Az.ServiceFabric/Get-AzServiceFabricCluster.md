---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279829"
---
# <span data-ttu-id="b4c44-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b4c44-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="b4c44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4c44-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c44-103">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4c44-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="b4c44-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4c44-104">SYNTAX</span></span>

### <span data-ttu-id="b4c44-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="b4c44-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c44-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4c44-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4c44-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b4c44-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4c44-108">說明</span><span class="sxs-lookup"><span data-stu-id="b4c44-108">DESCRIPTION</span></span>
<span data-ttu-id="b4c44-109">**AzServiceFabricCluster** 將會取得群集資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4c44-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="b4c44-110">示例</span><span class="sxs-lookup"><span data-stu-id="b4c44-110">EXAMPLES</span></span>

### <span data-ttu-id="b4c44-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b4c44-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="b4c44-112">這個命令會取得群集 ' myCluster」的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4c44-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="b4c44-113">參數</span><span class="sxs-lookup"><span data-stu-id="b4c44-113">PARAMETERS</span></span>

### <span data-ttu-id="b4c44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c44-114">-DefaultProfile</span></span>
<span data-ttu-id="b4c44-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4c44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c44-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4c44-116">-Name</span></span>
<span data-ttu-id="b4c44-117">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="b4c44-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b4c44-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c44-118">-ResourceGroupName</span></span>
<span data-ttu-id="b4c44-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4c44-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b4c44-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c44-120">CommonParameters</span></span>
<span data-ttu-id="b4c44-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4c44-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c44-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4c44-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c44-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b4c44-123">INPUTS</span></span>

### <span data-ttu-id="b4c44-124">System.object</span><span class="sxs-lookup"><span data-stu-id="b4c44-124">System.String</span></span>

## <span data-ttu-id="b4c44-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b4c44-125">OUTPUTS</span></span>

### <span data-ttu-id="b4c44-126">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="b4c44-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b4c44-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b4c44-127">NOTES</span></span>

## <span data-ttu-id="b4c44-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4c44-128">RELATED LINKS</span></span>
