---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456380"
---
# <span data-ttu-id="91043-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="91043-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="91043-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91043-102">SYNOPSIS</span></span>
<span data-ttu-id="91043-103">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91043-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91043-104">句法</span><span class="sxs-lookup"><span data-stu-id="91043-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91043-105">說明</span><span class="sxs-lookup"><span data-stu-id="91043-105">DESCRIPTION</span></span>
<span data-ttu-id="91043-106">[ **載入 AzureRmServiceFabricCluster** ] 會取得群集資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91043-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="91043-107">示例</span><span class="sxs-lookup"><span data-stu-id="91043-107">EXAMPLES</span></span>

### <span data-ttu-id="91043-108">範例1</span><span class="sxs-lookup"><span data-stu-id="91043-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="91043-109">這個命令會取得群集 ' myCluster」的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91043-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="91043-110">參數</span><span class="sxs-lookup"><span data-stu-id="91043-110">PARAMETERS</span></span>

### <span data-ttu-id="91043-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="91043-111">-Name</span></span>
<span data-ttu-id="91043-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="91043-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91043-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91043-113">-ResourceGroupName</span></span>
<span data-ttu-id="91043-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91043-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91043-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91043-115">-DefaultProfile</span></span>
<span data-ttu-id="91043-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91043-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91043-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91043-117">CommonParameters</span></span>
<span data-ttu-id="91043-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91043-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91043-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91043-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91043-120">輸入</span><span class="sxs-lookup"><span data-stu-id="91043-120">INPUTS</span></span>

### <span data-ttu-id="91043-121">System.object</span><span class="sxs-lookup"><span data-stu-id="91043-121">System.String</span></span>

## <span data-ttu-id="91043-122">輸出</span><span class="sxs-lookup"><span data-stu-id="91043-122">OUTPUTS</span></span>

### <span data-ttu-id="91043-123">ServiceFabric 集合. 泛型. IList "1 [PsCluster，ServiceFabric，Version = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = 非特定）</span><span class="sxs-lookup"><span data-stu-id="91043-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="91043-124">筆記</span><span class="sxs-lookup"><span data-stu-id="91043-124">NOTES</span></span>

## <span data-ttu-id="91043-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="91043-125">RELATED LINKS</span></span>

