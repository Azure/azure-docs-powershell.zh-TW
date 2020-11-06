---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452824"
---
# <span data-ttu-id="137e4-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="137e4-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="137e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="137e4-102">SYNOPSIS</span></span>
<span data-ttu-id="137e4-103">取得可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="137e4-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="137e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="137e4-104">SYNTAX</span></span>

### <span data-ttu-id="137e4-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="137e4-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="137e4-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="137e4-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="137e4-107">說明</span><span class="sxs-lookup"><span data-stu-id="137e4-107">DESCRIPTION</span></span>
<span data-ttu-id="137e4-108">**AzureRmCognitiveServicesAccountType** Cmdlet 會取得此訂閱下可用的認知服務帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="137e4-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="137e4-109">示例</span><span class="sxs-lookup"><span data-stu-id="137e4-109">EXAMPLES</span></span>

### <span data-ttu-id="137e4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="137e4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="137e4-111">取得可用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="137e4-111">Get the list of available Types.</span></span>

### <span data-ttu-id="137e4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="137e4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="137e4-113">在 westus 中取得可用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="137e4-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="137e4-114">範例3</span><span class="sxs-lookup"><span data-stu-id="137e4-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="137e4-115">檢查是否 `Face` 為有效的類型名稱，如果是有效的名稱，則會傳回名稱。</span><span class="sxs-lookup"><span data-stu-id="137e4-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="137e4-116">參數</span><span class="sxs-lookup"><span data-stu-id="137e4-116">PARAMETERS</span></span>

### <span data-ttu-id="137e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137e4-117">-DefaultProfile</span></span>
<span data-ttu-id="137e4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="137e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137e4-119">-位置</span><span class="sxs-lookup"><span data-stu-id="137e4-119">-Location</span></span>
<span data-ttu-id="137e4-120">認知服務帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="137e4-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="137e4-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="137e4-121">-TypeName</span></span>
<span data-ttu-id="137e4-122">認知服務帳戶類型名稱。</span><span class="sxs-lookup"><span data-stu-id="137e4-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="137e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137e4-123">CommonParameters</span></span>
<span data-ttu-id="137e4-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="137e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137e4-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="137e4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137e4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="137e4-126">INPUTS</span></span>

### <span data-ttu-id="137e4-127">System.object</span><span class="sxs-lookup"><span data-stu-id="137e4-127">System.String</span></span>

## <span data-ttu-id="137e4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="137e4-128">OUTPUTS</span></span>

### <span data-ttu-id="137e4-129">System.object []</span><span class="sxs-lookup"><span data-stu-id="137e4-129">System.String[]</span></span>

### <span data-ttu-id="137e4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="137e4-130">System.String</span></span>

## <span data-ttu-id="137e4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="137e4-131">NOTES</span></span>

## <span data-ttu-id="137e4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="137e4-132">RELATED LINKS</span></span>
