---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456420"
---
# <span data-ttu-id="085e8-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="085e8-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="085e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="085e8-102">SYNOPSIS</span></span>
<span data-ttu-id="085e8-103">檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="085e8-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="085e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="085e8-104">SYNTAX</span></span>

### <span data-ttu-id="085e8-105">ApplicationObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="085e8-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="085e8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="085e8-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="085e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="085e8-107">DESCRIPTION</span></span>
<span data-ttu-id="085e8-108">Get-AzureRmADAppCredential Cmdlet 可以用來檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="085e8-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="085e8-109">這個命令會檢索所有認證屬性 (但不會) 與應用程式相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="085e8-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="085e8-110">示例</span><span class="sxs-lookup"><span data-stu-id="085e8-110">EXAMPLES</span></span>

### <span data-ttu-id="085e8-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="085e8-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="085e8-112">傳回與含物件 id ' 1f99cf81-0146-4f4e-beae-2007d0668476」之應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="085e8-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="085e8-113">參數</span><span class="sxs-lookup"><span data-stu-id="085e8-113">PARAMETERS</span></span>

### <span data-ttu-id="085e8-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="085e8-114">-ApplicationId</span></span>
<span data-ttu-id="085e8-115">要從中檢索認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="085e8-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="085e8-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="085e8-116">-ObjectId</span></span>
<span data-ttu-id="085e8-117">要從中檢索認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="085e8-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="085e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085e8-118">-DefaultProfile</span></span>
<span data-ttu-id="085e8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="085e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="085e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085e8-120">CommonParameters</span></span>
<span data-ttu-id="085e8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="085e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085e8-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="085e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085e8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="085e8-123">INPUTS</span></span>

## <span data-ttu-id="085e8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="085e8-124">OUTPUTS</span></span>

### <span data-ttu-id="085e8-125">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="085e8-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="085e8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="085e8-126">NOTES</span></span>

## <span data-ttu-id="085e8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="085e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="085e8-128">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="085e8-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="085e8-129">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="085e8-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="085e8-130">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="085e8-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

