---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958065"
---
# <span data-ttu-id="a981d-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="a981d-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="a981d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a981d-102">SYNOPSIS</span></span>
<span data-ttu-id="a981d-103">取得可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a981d-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="a981d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a981d-104">SYNTAX</span></span>

### <span data-ttu-id="a981d-105">GetAccountTypes (預設) </span><span class="sxs-lookup"><span data-stu-id="a981d-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a981d-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="a981d-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a981d-107">說明</span><span class="sxs-lookup"><span data-stu-id="a981d-107">DESCRIPTION</span></span>
<span data-ttu-id="a981d-108">**AzCognitiveServicesAccountType** Cmdlet 會取得此訂閱下可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a981d-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="a981d-109">示例</span><span class="sxs-lookup"><span data-stu-id="a981d-109">EXAMPLES</span></span>

### <span data-ttu-id="a981d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a981d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="a981d-111">取得可用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="a981d-111">Get the list of available Types.</span></span>

### <span data-ttu-id="a981d-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a981d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="a981d-113">在 westus 中取得可用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="a981d-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="a981d-114">範例3</span><span class="sxs-lookup"><span data-stu-id="a981d-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="a981d-115">檢查是否 `Face` 為有效的類型名稱，如果是有效的名稱，則會傳回名稱。</span><span class="sxs-lookup"><span data-stu-id="a981d-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="a981d-116">參數</span><span class="sxs-lookup"><span data-stu-id="a981d-116">PARAMETERS</span></span>

### <span data-ttu-id="a981d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a981d-117">-DefaultProfile</span></span>
<span data-ttu-id="a981d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a981d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a981d-119">-位置</span><span class="sxs-lookup"><span data-stu-id="a981d-119">-Location</span></span>
<span data-ttu-id="a981d-120">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="a981d-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="a981d-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="a981d-121">-TypeName</span></span>
<span data-ttu-id="a981d-122">認知服務帳戶類型名稱。</span><span class="sxs-lookup"><span data-stu-id="a981d-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="a981d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a981d-123">CommonParameters</span></span>
<span data-ttu-id="a981d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a981d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a981d-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a981d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a981d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a981d-126">INPUTS</span></span>

### <span data-ttu-id="a981d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="a981d-127">System.String</span></span>

## <span data-ttu-id="a981d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a981d-128">OUTPUTS</span></span>

### <span data-ttu-id="a981d-129">System.object []</span><span class="sxs-lookup"><span data-stu-id="a981d-129">System.String[]</span></span>

### <span data-ttu-id="a981d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a981d-130">System.String</span></span>

## <span data-ttu-id="a981d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a981d-131">NOTES</span></span>

## <span data-ttu-id="a981d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a981d-132">RELATED LINKS</span></span>
