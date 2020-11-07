---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623918"
---
# <span data-ttu-id="b765a-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b765a-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="b765a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b765a-102">SYNOPSIS</span></span>
<span data-ttu-id="b765a-103">取得公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="b765a-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b765a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b765a-104">SYNTAX</span></span>

### <span data-ttu-id="b765a-105"> (預設) </span><span class="sxs-lookup"><span data-stu-id="b765a-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b765a-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b765a-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b765a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b765a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b765a-108">說明</span><span class="sxs-lookup"><span data-stu-id="b765a-108">DESCRIPTION</span></span>
<span data-ttu-id="b765a-109">**AzureRmPublicIpPrefix** Cmdlet 會取得資源群組中的一個或多個公用 IP 首碼。</span><span class="sxs-lookup"><span data-stu-id="b765a-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="b765a-110">示例</span><span class="sxs-lookup"><span data-stu-id="b765a-110">EXAMPLES</span></span>

### <span data-ttu-id="b765a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b765a-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="b765a-112">這個命令會以資源群組 $rgName 中的 $prefixName 取得公用 IP 首碼資源</span><span class="sxs-lookup"><span data-stu-id="b765a-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="b765a-113">參數</span><span class="sxs-lookup"><span data-stu-id="b765a-113">PARAMETERS</span></span>

### <span data-ttu-id="b765a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b765a-114">-DefaultProfile</span></span>
<span data-ttu-id="b765a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b765a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b765a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b765a-116">-Name</span></span>
<span data-ttu-id="b765a-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b765a-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b765a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b765a-118">-ResourceGroupName</span></span>
<span data-ttu-id="b765a-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b765a-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b765a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b765a-120">-ResourceId</span></span>
<span data-ttu-id="b765a-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b765a-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b765a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b765a-122">CommonParameters</span></span>
<span data-ttu-id="b765a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b765a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b765a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b765a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b765a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b765a-125">INPUTS</span></span>

### <span data-ttu-id="b765a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b765a-126">System.String</span></span>


## <span data-ttu-id="b765a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b765a-127">OUTPUTS</span></span>

### <span data-ttu-id="b765a-128">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b765a-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="b765a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b765a-129">NOTES</span></span>

## <span data-ttu-id="b765a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b765a-130">RELATED LINKS</span></span>
