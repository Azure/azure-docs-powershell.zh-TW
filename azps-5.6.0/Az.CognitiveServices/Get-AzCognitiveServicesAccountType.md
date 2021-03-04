---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909226"
---
# <span data-ttu-id="5c683-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="5c683-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="5c683-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c683-102">SYNOPSIS</span></span>
<span data-ttu-id="5c683-103">獲得可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="5c683-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="5c683-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c683-104">SYNTAX</span></span>

### <span data-ttu-id="5c683-105">GetAccountTypes (預設) </span><span class="sxs-lookup"><span data-stu-id="5c683-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c683-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="5c683-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c683-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c683-107">DESCRIPTION</span></span>
<span data-ttu-id="5c683-108">**Get-AzCognitiveServicesAccountType** Cmdlet 會在此訂閱下取得可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="5c683-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="5c683-109">例子</span><span class="sxs-lookup"><span data-stu-id="5c683-109">EXAMPLES</span></span>

### <span data-ttu-id="5c683-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c683-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="5c683-111">取得可用類型清單。</span><span class="sxs-lookup"><span data-stu-id="5c683-111">Get the list of available Types.</span></span>

### <span data-ttu-id="5c683-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="5c683-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="5c683-113">取得 westus 中可用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="5c683-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="5c683-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="5c683-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="5c683-115">檢查是否為有效的類型名稱，如果該名稱是有效的名稱， `Face` 將會返回該名稱。</span><span class="sxs-lookup"><span data-stu-id="5c683-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="5c683-116">參數</span><span class="sxs-lookup"><span data-stu-id="5c683-116">PARAMETERS</span></span>

### <span data-ttu-id="5c683-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c683-117">-DefaultProfile</span></span>
<span data-ttu-id="5c683-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c683-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c683-119">-位置</span><span class="sxs-lookup"><span data-stu-id="5c683-119">-Location</span></span>
<span data-ttu-id="5c683-120">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="5c683-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c683-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="5c683-121">-TypeName</span></span>
<span data-ttu-id="5c683-122">認知服務帳戶類型名稱。</span><span class="sxs-lookup"><span data-stu-id="5c683-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c683-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c683-123">CommonParameters</span></span>
<span data-ttu-id="5c683-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c683-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c683-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c683-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c683-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5c683-126">INPUTS</span></span>

### <span data-ttu-id="5c683-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c683-127">System.String</span></span>

## <span data-ttu-id="5c683-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5c683-128">OUTPUTS</span></span>

### <span data-ttu-id="5c683-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5c683-129">System.String[]</span></span>

### <span data-ttu-id="5c683-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5c683-130">System.String</span></span>

## <span data-ttu-id="5c683-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5c683-131">NOTES</span></span>

## <span data-ttu-id="5c683-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c683-132">RELATED LINKS</span></span>
