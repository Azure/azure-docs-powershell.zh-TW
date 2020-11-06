---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446682"
---
# <span data-ttu-id="2f539-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2f539-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="2f539-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f539-102">SYNOPSIS</span></span>
<span data-ttu-id="2f539-103">檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="2f539-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f539-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f539-104">SYNTAX</span></span>

### <span data-ttu-id="2f539-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2f539-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f539-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f539-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f539-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f539-107">DESCRIPTION</span></span>
<span data-ttu-id="2f539-108">Get-AzureRmADSpCredential Cmdlet 可以用來檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="2f539-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="2f539-109">這個命令會檢索所有認證屬性 (但不會) 與服務主體相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="2f539-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="2f539-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f539-110">EXAMPLES</span></span>

### <span data-ttu-id="2f539-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f539-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="2f539-112">傳回與包含 SPN '」之服務主體相關聯的認證清單 http://test12345 。</span><span class="sxs-lookup"><span data-stu-id="2f539-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="2f539-113">參數</span><span class="sxs-lookup"><span data-stu-id="2f539-113">PARAMETERS</span></span>

### <span data-ttu-id="2f539-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2f539-114">-ObjectId</span></span>
<span data-ttu-id="2f539-115">要從中檢索認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f539-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f539-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2f539-116">-ServicePrincipalName</span></span>
<span data-ttu-id="2f539-117">要從中檢索認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f539-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f539-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f539-118">-DefaultProfile</span></span>
<span data-ttu-id="2f539-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f539-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f539-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f539-120">CommonParameters</span></span>
<span data-ttu-id="2f539-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f539-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f539-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f539-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f539-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2f539-123">INPUTS</span></span>

## <span data-ttu-id="2f539-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2f539-124">OUTPUTS</span></span>

### <span data-ttu-id="2f539-125">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2f539-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2f539-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2f539-126">NOTES</span></span>

## <span data-ttu-id="2f539-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f539-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f539-128">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2f539-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="2f539-129">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2f539-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="2f539-130">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2f539-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

