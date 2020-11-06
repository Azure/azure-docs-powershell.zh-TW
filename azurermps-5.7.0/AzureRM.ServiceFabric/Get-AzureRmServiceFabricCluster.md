---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446011"
---
# <span data-ttu-id="10d28-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="10d28-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="10d28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10d28-102">SYNOPSIS</span></span>
<span data-ttu-id="10d28-103">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="10d28-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d28-104">句法</span><span class="sxs-lookup"><span data-stu-id="10d28-104">SYNTAX</span></span>

### <span data-ttu-id="10d28-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="10d28-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d28-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10d28-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10d28-107">ByName</span><span class="sxs-lookup"><span data-stu-id="10d28-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d28-108">說明</span><span class="sxs-lookup"><span data-stu-id="10d28-108">DESCRIPTION</span></span>
<span data-ttu-id="10d28-109">[ **載入 AzureRmServiceFabricCluster** ] 會取得群集資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="10d28-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="10d28-110">示例</span><span class="sxs-lookup"><span data-stu-id="10d28-110">EXAMPLES</span></span>

### <span data-ttu-id="10d28-111">範例1</span><span class="sxs-lookup"><span data-stu-id="10d28-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="10d28-112">這個命令會取得群集 ' myCluster」的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="10d28-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="10d28-113">參數</span><span class="sxs-lookup"><span data-stu-id="10d28-113">PARAMETERS</span></span>

### <span data-ttu-id="10d28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d28-114">-DefaultProfile</span></span>
<span data-ttu-id="10d28-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10d28-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d28-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="10d28-116">-Name</span></span>
<span data-ttu-id="10d28-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="10d28-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10d28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d28-118">-ResourceGroupName</span></span>
<span data-ttu-id="10d28-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10d28-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10d28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d28-120">CommonParameters</span></span>
<span data-ttu-id="10d28-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10d28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d28-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10d28-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d28-123">輸入</span><span class="sxs-lookup"><span data-stu-id="10d28-123">INPUTS</span></span>

### <span data-ttu-id="10d28-124">System.object</span><span class="sxs-lookup"><span data-stu-id="10d28-124">System.String</span></span>

## <span data-ttu-id="10d28-125">輸出</span><span class="sxs-lookup"><span data-stu-id="10d28-125">OUTPUTS</span></span>

### <span data-ttu-id="10d28-126">ServiceFabric 集合. 泛型. IList "1 [PsCluster，ServiceFabric，Version = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = 非特定）</span><span class="sxs-lookup"><span data-stu-id="10d28-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10d28-127">筆記</span><span class="sxs-lookup"><span data-stu-id="10d28-127">NOTES</span></span>

## <span data-ttu-id="10d28-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="10d28-128">RELATED LINKS</span></span>

