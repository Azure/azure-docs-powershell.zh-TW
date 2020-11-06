---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452712"
---
# <span data-ttu-id="c3c79-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c3c79-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="c3c79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3c79-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c79-103">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3c79-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3c79-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3c79-104">SYNTAX</span></span>

### <span data-ttu-id="c3c79-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="c3c79-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3c79-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c3c79-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3c79-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c3c79-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c79-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3c79-108">DESCRIPTION</span></span>
<span data-ttu-id="c3c79-109">**AzureRmServiceFabricCluster** 將會取得群集資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3c79-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="c3c79-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3c79-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c79-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c3c79-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="c3c79-112">這個命令會取得群集 ' myCluster」的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3c79-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="c3c79-113">參數</span><span class="sxs-lookup"><span data-stu-id="c3c79-113">PARAMETERS</span></span>

### <span data-ttu-id="c3c79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c79-114">-DefaultProfile</span></span>
<span data-ttu-id="c3c79-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3c79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3c79-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3c79-116">-Name</span></span>
<span data-ttu-id="c3c79-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3c79-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c3c79-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c79-118">-ResourceGroupName</span></span>
<span data-ttu-id="c3c79-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3c79-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c3c79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c79-120">CommonParameters</span></span>
<span data-ttu-id="c3c79-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3c79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c79-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3c79-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c79-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c3c79-123">INPUTS</span></span>

### <span data-ttu-id="c3c79-124">System.object</span><span class="sxs-lookup"><span data-stu-id="c3c79-124">System.String</span></span>

## <span data-ttu-id="c3c79-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c3c79-125">OUTPUTS</span></span>

### <span data-ttu-id="c3c79-126">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="c3c79-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c3c79-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c3c79-127">NOTES</span></span>

## <span data-ttu-id="c3c79-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3c79-128">RELATED LINKS</span></span>
