---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446640"
---
# <span data-ttu-id="7baeb-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7baeb-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="7baeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7baeb-102">SYNOPSIS</span></span>
<span data-ttu-id="7baeb-103">取得 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="7baeb-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="7baeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="7baeb-104">SYNTAX</span></span>

### <span data-ttu-id="7baeb-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7baeb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7baeb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7baeb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7baeb-107">說明</span><span class="sxs-lookup"><span data-stu-id="7baeb-107">DESCRIPTION</span></span>
<span data-ttu-id="7baeb-108">Get-AzCdnOriginGroup Cmdlet 會檢索 CDN 來源群組。</span><span class="sxs-lookup"><span data-stu-id="7baeb-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="7baeb-109">示例</span><span class="sxs-lookup"><span data-stu-id="7baeb-109">EXAMPLES</span></span>

### <span data-ttu-id="7baeb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7baeb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="7baeb-111">這個命令會在指定的端點中取得原點群組。</span><span class="sxs-lookup"><span data-stu-id="7baeb-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="7baeb-112">參數</span><span class="sxs-lookup"><span data-stu-id="7baeb-112">PARAMETERS</span></span>

### <span data-ttu-id="7baeb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baeb-113">-DefaultProfile</span></span>
<span data-ttu-id="7baeb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7baeb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7baeb-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="7baeb-115">-EndpointName</span></span>
<span data-ttu-id="7baeb-116">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="7baeb-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7baeb-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="7baeb-117">-OriginGroupName</span></span>
<span data-ttu-id="7baeb-118">Azure CDN 原始組名。</span><span class="sxs-lookup"><span data-stu-id="7baeb-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="7baeb-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7baeb-119">-ProfileName</span></span>
<span data-ttu-id="7baeb-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7baeb-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7baeb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7baeb-121">-ResourceGroupName</span></span>
<span data-ttu-id="7baeb-122">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="7baeb-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7baeb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7baeb-123">-ResourceId</span></span>
<span data-ttu-id="7baeb-124">來源群組的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7baeb-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="7baeb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baeb-125">CommonParameters</span></span>
<span data-ttu-id="7baeb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7baeb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baeb-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7baeb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baeb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7baeb-128">INPUTS</span></span>

### <span data-ttu-id="7baeb-129">所有</span><span class="sxs-lookup"><span data-stu-id="7baeb-129">None</span></span>

## <span data-ttu-id="7baeb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7baeb-130">OUTPUTS</span></span>

### <span data-ttu-id="7baeb-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7baeb-131">System.Object</span></span>

## <span data-ttu-id="7baeb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7baeb-132">NOTES</span></span>

## <span data-ttu-id="7baeb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7baeb-133">RELATED LINKS</span></span>
