---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448007"
---
# <span data-ttu-id="26208-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26208-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="26208-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26208-102">SYNOPSIS</span></span>
<span data-ttu-id="26208-103">搜尋資源群組。</span><span class="sxs-lookup"><span data-stu-id="26208-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26208-104">句法</span><span class="sxs-lookup"><span data-stu-id="26208-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26208-105">說明</span><span class="sxs-lookup"><span data-stu-id="26208-105">DESCRIPTION</span></span>
<span data-ttu-id="26208-106">**AzureRmResourceGroup** Cmdlet 會使用指定的參數搜尋資源群組。</span><span class="sxs-lookup"><span data-stu-id="26208-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="26208-107">示例</span><span class="sxs-lookup"><span data-stu-id="26208-107">EXAMPLES</span></span>

### <span data-ttu-id="26208-108">範例1：尋找所有資源群組</span><span class="sxs-lookup"><span data-stu-id="26208-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="26208-109">這個命令會找出所有的資源群組。</span><span class="sxs-lookup"><span data-stu-id="26208-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="26208-110">範例2：依標記名稱尋找資源群組</span><span class="sxs-lookup"><span data-stu-id="26208-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="26208-111">這個命令會找出所有擁有名為 testtag 的標籤的資源群組。</span><span class="sxs-lookup"><span data-stu-id="26208-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="26208-112">範例3：依標記名稱和值尋找資源群組</span><span class="sxs-lookup"><span data-stu-id="26208-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="26208-113">這個命令會找出所有名為 testtag 的標籤和值 testval 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="26208-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="26208-114">參數</span><span class="sxs-lookup"><span data-stu-id="26208-114">PARAMETERS</span></span>

### <span data-ttu-id="26208-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26208-115">-ApiVersion</span></span>
<span data-ttu-id="26208-116">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="26208-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="26208-117">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="26208-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26208-118">-預先</span><span class="sxs-lookup"><span data-stu-id="26208-118">-Pre</span></span>
<span data-ttu-id="26208-119">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="26208-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26208-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="26208-120">-Tag</span></span>
<span data-ttu-id="26208-121">指定標記資訊（做為雜湊資料表）來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="26208-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="26208-122">使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="26208-122">Use the following formats:</span></span>

<span data-ttu-id="26208-123">@ {tagName = $null} 或 @ {tagName = "tagValue"}。</span><span class="sxs-lookup"><span data-stu-id="26208-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26208-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26208-124">-DefaultProfile</span></span>
<span data-ttu-id="26208-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26208-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26208-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26208-126">CommonParameters</span></span>
<span data-ttu-id="26208-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26208-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26208-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26208-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26208-129">輸入</span><span class="sxs-lookup"><span data-stu-id="26208-129">INPUTS</span></span>

## <span data-ttu-id="26208-130">輸出</span><span class="sxs-lookup"><span data-stu-id="26208-130">OUTPUTS</span></span>

### <span data-ttu-id="26208-131">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="26208-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="26208-132">筆記</span><span class="sxs-lookup"><span data-stu-id="26208-132">NOTES</span></span>

## <span data-ttu-id="26208-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="26208-133">RELATED LINKS</span></span>

