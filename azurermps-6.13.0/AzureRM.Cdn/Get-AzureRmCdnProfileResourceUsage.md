---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445683"
---
# <span data-ttu-id="9ed56-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="9ed56-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="9ed56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ed56-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed56-103">取得 CDN 設定檔的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="9ed56-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed56-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ed56-104">SYNTAX</span></span>

### <span data-ttu-id="9ed56-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ed56-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed56-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ed56-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ed56-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ed56-107">DESCRIPTION</span></span>
<span data-ttu-id="9ed56-108">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="9ed56-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9ed56-109">示例</span><span class="sxs-lookup"><span data-stu-id="9ed56-109">EXAMPLES</span></span>

### <span data-ttu-id="9ed56-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9ed56-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9ed56-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="9ed56-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="9ed56-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ed56-112">PARAMETERS</span></span>

### <span data-ttu-id="9ed56-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ed56-113">-CdnProfile</span></span>
<span data-ttu-id="9ed56-114">Azure CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="9ed56-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="9ed56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed56-115">-DefaultProfile</span></span>
<span data-ttu-id="9ed56-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9ed56-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ed56-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9ed56-117">-ProfileName</span></span>
<span data-ttu-id="9ed56-118">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed56-118">The name of the profile.</span></span>

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

### <span data-ttu-id="9ed56-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed56-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ed56-120">設定檔所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9ed56-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="9ed56-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed56-121">CommonParameters</span></span>
<span data-ttu-id="9ed56-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ed56-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed56-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ed56-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed56-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9ed56-124">INPUTS</span></span>

### <span data-ttu-id="9ed56-125">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ed56-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="9ed56-126">參數： CdnProfile (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9ed56-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="9ed56-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9ed56-127">OUTPUTS</span></span>

### <span data-ttu-id="9ed56-128">PSResourceUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ed56-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="9ed56-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9ed56-129">NOTES</span></span>

## <span data-ttu-id="9ed56-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ed56-130">RELATED LINKS</span></span>
