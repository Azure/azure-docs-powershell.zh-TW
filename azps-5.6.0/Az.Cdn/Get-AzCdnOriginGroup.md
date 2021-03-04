---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: f79b3b4e8347c485230141416461c1f320d3d7b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913598"
---
# <span data-ttu-id="3efc2-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="3efc2-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="3efc2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3efc2-102">SYNOPSIS</span></span>
<span data-ttu-id="3efc2-103">獲得 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="3efc2-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="3efc2-104">語法</span><span class="sxs-lookup"><span data-stu-id="3efc2-104">SYNTAX</span></span>

### <span data-ttu-id="3efc2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3efc2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3efc2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3efc2-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3efc2-107">描述</span><span class="sxs-lookup"><span data-stu-id="3efc2-107">DESCRIPTION</span></span>
<span data-ttu-id="3efc2-108">Cmdlet Get-AzCdnOriginGroup會取回 CDN 來源群組。</span><span class="sxs-lookup"><span data-stu-id="3efc2-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="3efc2-109">例子</span><span class="sxs-lookup"><span data-stu-id="3efc2-109">EXAMPLES</span></span>

### <span data-ttu-id="3efc2-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3efc2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="3efc2-111">此命令會取得指定端點內的原始群組。</span><span class="sxs-lookup"><span data-stu-id="3efc2-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="3efc2-112">參數</span><span class="sxs-lookup"><span data-stu-id="3efc2-112">PARAMETERS</span></span>

### <span data-ttu-id="3efc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efc2-113">-DefaultProfile</span></span>
<span data-ttu-id="3efc2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3efc2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3efc2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3efc2-115">-EndpointName</span></span>
<span data-ttu-id="3efc2-116">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="3efc2-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="3efc2-117">-OriginGroupName</span></span>
<span data-ttu-id="3efc2-118">Azure CDN 來源組名。</span><span class="sxs-lookup"><span data-stu-id="3efc2-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3efc2-119">-ProfileName</span></span>
<span data-ttu-id="3efc2-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3efc2-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3efc2-121">-ResourceGroupName</span></span>
<span data-ttu-id="3efc2-122">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3efc2-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3efc2-123">-ResourceId</span></span>
<span data-ttu-id="3efc2-124">來源群組的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3efc2-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efc2-125">CommonParameters</span></span>
<span data-ttu-id="3efc2-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3efc2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efc2-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3efc2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efc2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3efc2-128">INPUTS</span></span>

### <span data-ttu-id="3efc2-129">沒有</span><span class="sxs-lookup"><span data-stu-id="3efc2-129">None</span></span>

## <span data-ttu-id="3efc2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3efc2-130">OUTPUTS</span></span>

### <span data-ttu-id="3efc2-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="3efc2-131">System.Object</span></span>

## <span data-ttu-id="3efc2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3efc2-132">NOTES</span></span>

## <span data-ttu-id="3efc2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3efc2-133">RELATED LINKS</span></span>
