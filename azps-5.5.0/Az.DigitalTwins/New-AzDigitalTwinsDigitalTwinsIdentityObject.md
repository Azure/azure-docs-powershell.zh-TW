---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143187"
---
# <span data-ttu-id="93312-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="93312-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="93312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93312-102">SYNOPSIS</span></span>
<span data-ttu-id="93312-103">為 DigitalTwinsIdentity 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="93312-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93312-104">句法</span><span class="sxs-lookup"><span data-stu-id="93312-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="93312-105">說明</span><span class="sxs-lookup"><span data-stu-id="93312-105">DESCRIPTION</span></span>
<span data-ttu-id="93312-106">為 DigitalTwinsIdentity 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="93312-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93312-107">示例</span><span class="sxs-lookup"><span data-stu-id="93312-107">EXAMPLES</span></span>

### <span data-ttu-id="93312-108">範例1：建立 DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="93312-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="93312-109">依識別碼和位置建立 DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="93312-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="93312-110">參數</span><span class="sxs-lookup"><span data-stu-id="93312-110">PARAMETERS</span></span>

### <span data-ttu-id="93312-111">-終結點</span><span class="sxs-lookup"><span data-stu-id="93312-111">-EndpointName</span></span>
<span data-ttu-id="93312-112">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="93312-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="93312-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="93312-113">-Id</span></span>
<span data-ttu-id="93312-114">資源身分識別路徑。</span><span class="sxs-lookup"><span data-stu-id="93312-114">Resource identity path.</span></span>

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

### <span data-ttu-id="93312-115">-位置</span><span class="sxs-lookup"><span data-stu-id="93312-115">-Location</span></span>
<span data-ttu-id="93312-116">DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="93312-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93312-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93312-117">-ResourceGroupName</span></span>
<span data-ttu-id="93312-118">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93312-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93312-119">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="93312-119">-ResourceName</span></span>
<span data-ttu-id="93312-120">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="93312-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="93312-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93312-121">-SubscriptionId</span></span>
<span data-ttu-id="93312-122">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="93312-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="93312-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93312-123">CommonParameters</span></span>
<span data-ttu-id="93312-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93312-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93312-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93312-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93312-126">輸入</span><span class="sxs-lookup"><span data-stu-id="93312-126">INPUTS</span></span>

## <span data-ttu-id="93312-127">輸出</span><span class="sxs-lookup"><span data-stu-id="93312-127">OUTPUTS</span></span>

### <span data-ttu-id="93312-128">DigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="93312-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="93312-129">筆記</span><span class="sxs-lookup"><span data-stu-id="93312-129">NOTES</span></span>

<span data-ttu-id="93312-130">別名</span><span class="sxs-lookup"><span data-stu-id="93312-130">ALIASES</span></span>

## <span data-ttu-id="93312-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="93312-131">RELATED LINKS</span></span>

