---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457408"
---
# <span data-ttu-id="f3d16-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f3d16-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="f3d16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3d16-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d16-103">取得現有的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="f3d16-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d16-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3d16-104">SYNTAX</span></span>

### <span data-ttu-id="f3d16-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="f3d16-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d16-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d16-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d16-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d16-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d16-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d16-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d16-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3d16-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d16-110">說明</span><span class="sxs-lookup"><span data-stu-id="f3d16-110">DESCRIPTION</span></span>
<span data-ttu-id="f3d16-111">**AzureRmNetworkProfile** Cmdlet 會檢索現有的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="f3d16-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="f3d16-112">示例</span><span class="sxs-lookup"><span data-stu-id="f3d16-112">EXAMPLES</span></span>

### <span data-ttu-id="f3d16-113">範例1</span><span class="sxs-lookup"><span data-stu-id="f3d16-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="f3d16-114">這會在資源群組 rg1 中檢索網路設定檔 np1</span><span class="sxs-lookup"><span data-stu-id="f3d16-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="f3d16-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3d16-115">PARAMETERS</span></span>

### <span data-ttu-id="f3d16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d16-116">-DefaultProfile</span></span>
<span data-ttu-id="f3d16-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3d16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d16-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f3d16-118">-ExpandResource</span></span>
<span data-ttu-id="f3d16-119">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="f3d16-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d16-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3d16-120">-Name</span></span>
<span data-ttu-id="f3d16-121">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d16-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d16-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3d16-123">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f3d16-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d16-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3d16-124">-ResourceId</span></span>
<span data-ttu-id="f3d16-125">網路設定檔的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3d16-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d16-126">CommonParameters</span></span>
<span data-ttu-id="f3d16-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3d16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d16-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3d16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d16-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f3d16-129">INPUTS</span></span>

### <span data-ttu-id="f3d16-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f3d16-130">System.String</span></span>

## <span data-ttu-id="f3d16-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f3d16-131">OUTPUTS</span></span>

### <span data-ttu-id="f3d16-132">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3d16-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f3d16-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f3d16-133">NOTES</span></span>

## <span data-ttu-id="f3d16-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3d16-134">RELATED LINKS</span></span>
