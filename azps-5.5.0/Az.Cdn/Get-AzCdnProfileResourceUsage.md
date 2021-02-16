---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141403"
---
# <span data-ttu-id="70f20-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="70f20-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="70f20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70f20-102">SYNOPSIS</span></span>
<span data-ttu-id="70f20-103">取得 CDN 設定檔的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="70f20-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="70f20-104">句法</span><span class="sxs-lookup"><span data-stu-id="70f20-104">SYNTAX</span></span>

### <span data-ttu-id="70f20-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70f20-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70f20-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70f20-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70f20-107">說明</span><span class="sxs-lookup"><span data-stu-id="70f20-107">DESCRIPTION</span></span>
<span data-ttu-id="70f20-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="70f20-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="70f20-109">示例</span><span class="sxs-lookup"><span data-stu-id="70f20-109">EXAMPLES</span></span>

### <span data-ttu-id="70f20-110">範例1</span><span class="sxs-lookup"><span data-stu-id="70f20-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="70f20-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="70f20-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="70f20-112">參數</span><span class="sxs-lookup"><span data-stu-id="70f20-112">PARAMETERS</span></span>

### <span data-ttu-id="70f20-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="70f20-113">-CdnProfile</span></span>
<span data-ttu-id="70f20-114">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="70f20-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f20-115">-DefaultProfile</span></span>
<span data-ttu-id="70f20-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="70f20-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70f20-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="70f20-117">-ProfileName</span></span>
<span data-ttu-id="70f20-118">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="70f20-118">The name of the profile.</span></span>

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

### <span data-ttu-id="70f20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f20-119">-ResourceGroupName</span></span>
<span data-ttu-id="70f20-120">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="70f20-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="70f20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f20-121">CommonParameters</span></span>
<span data-ttu-id="70f20-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70f20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f20-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70f20-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f20-124">輸入</span><span class="sxs-lookup"><span data-stu-id="70f20-124">INPUTS</span></span>

### <span data-ttu-id="70f20-125">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70f20-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="70f20-126">輸出</span><span class="sxs-lookup"><span data-stu-id="70f20-126">OUTPUTS</span></span>

### <span data-ttu-id="70f20-127">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70f20-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="70f20-128">筆記</span><span class="sxs-lookup"><span data-stu-id="70f20-128">NOTES</span></span>

## <span data-ttu-id="70f20-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="70f20-129">RELATED LINKS</span></span>
