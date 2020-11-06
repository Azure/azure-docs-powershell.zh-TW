---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448572"
---
# <span data-ttu-id="64664-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64664-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="64664-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64664-102">SYNOPSIS</span></span>
<span data-ttu-id="64664-103">檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="64664-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64664-104">句法</span><span class="sxs-lookup"><span data-stu-id="64664-104">SYNTAX</span></span>

### <span data-ttu-id="64664-105">ApplicationObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="64664-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64664-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64664-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64664-107">說明</span><span class="sxs-lookup"><span data-stu-id="64664-107">DESCRIPTION</span></span>
<span data-ttu-id="64664-108">Get-AzureRmADAppCredential Cmdlet 可以用來檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="64664-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="64664-109">這個命令會檢索所有認證屬性 (但不會) 與應用程式相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="64664-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="64664-110">示例</span><span class="sxs-lookup"><span data-stu-id="64664-110">EXAMPLES</span></span>

### <span data-ttu-id="64664-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64664-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="64664-112">傳回與含物件 id ' 1f99cf81-0146-4f4e-beae-2007d0668476」之應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="64664-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="64664-113">參數</span><span class="sxs-lookup"><span data-stu-id="64664-113">PARAMETERS</span></span>

### <span data-ttu-id="64664-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="64664-114">-ApplicationId</span></span>
<span data-ttu-id="64664-115">要從中檢索認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="64664-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64664-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64664-116">-DefaultProfile</span></span>
<span data-ttu-id="64664-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="64664-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64664-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="64664-118">-ObjectId</span></span>
<span data-ttu-id="64664-119">要從中檢索認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="64664-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64664-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64664-120">CommonParameters</span></span>
<span data-ttu-id="64664-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64664-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64664-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64664-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64664-123">輸入</span><span class="sxs-lookup"><span data-stu-id="64664-123">INPUTS</span></span>

### <span data-ttu-id="64664-124">所有</span><span class="sxs-lookup"><span data-stu-id="64664-124">None</span></span>
<span data-ttu-id="64664-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="64664-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64664-126">輸出</span><span class="sxs-lookup"><span data-stu-id="64664-126">OUTPUTS</span></span>

### <span data-ttu-id="64664-127">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="64664-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="64664-128">筆記</span><span class="sxs-lookup"><span data-stu-id="64664-128">NOTES</span></span>

## <span data-ttu-id="64664-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="64664-129">RELATED LINKS</span></span>

[<span data-ttu-id="64664-130">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64664-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="64664-131">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64664-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="64664-132">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64664-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

