---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 72a2510c673d0e68fc3820fda7b1d99e15a6aa76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448937"
---
# <span data-ttu-id="dffb5-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dffb5-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="dffb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dffb5-102">SYNOPSIS</span></span>
<span data-ttu-id="dffb5-103">檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="dffb5-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dffb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="dffb5-104">SYNTAX</span></span>

### <span data-ttu-id="dffb5-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dffb5-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffb5-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dffb5-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dffb5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dffb5-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffb5-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dffb5-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dffb5-109">說明</span><span class="sxs-lookup"><span data-stu-id="dffb5-109">DESCRIPTION</span></span>
<span data-ttu-id="dffb5-110">Get-AzureRmADSpCredential Cmdlet 可以用來檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="dffb5-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="dffb5-111">這個命令會檢索所有認證屬性 (但不會) 與服務主體相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="dffb5-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="dffb5-112">示例</span><span class="sxs-lookup"><span data-stu-id="dffb5-112">EXAMPLES</span></span>

### <span data-ttu-id="dffb5-113">範例 1-依 SPN 列出認證</span><span class="sxs-lookup"><span data-stu-id="dffb5-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="dffb5-114">使用 SPN "" 傳回與服務主體相關聯的認證清單 http://test12345 。</span><span class="sxs-lookup"><span data-stu-id="dffb5-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="dffb5-115">範例 2-依物件識別碼列出認證</span><span class="sxs-lookup"><span data-stu-id="dffb5-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="dffb5-116">使用物件 id "58e28616-99cc-4da4-b705-7672130e1047" 傳回與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="dffb5-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="dffb5-117">範例 3-依管道列出認證</span><span class="sxs-lookup"><span data-stu-id="dffb5-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="dffb5-118">取得物件識別碼為 "58e28616-99cc-4da4-b705-7672130e1047" 的服務主體，並將其管道至 Get-AzureRmADSpCredential Cmdlet，以列出該服務主體的所有認證。</span><span class="sxs-lookup"><span data-stu-id="dffb5-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="dffb5-119">參數</span><span class="sxs-lookup"><span data-stu-id="dffb5-119">PARAMETERS</span></span>

### <span data-ttu-id="dffb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffb5-120">-DefaultProfile</span></span>
<span data-ttu-id="dffb5-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dffb5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dffb5-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dffb5-122">-DisplayName</span></span>
<span data-ttu-id="dffb5-123">服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dffb5-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dffb5-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dffb5-124">-ObjectId</span></span>
<span data-ttu-id="dffb5-125">要從中檢索認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="dffb5-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dffb5-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dffb5-126">-ServicePrincipalName</span></span>
<span data-ttu-id="dffb5-127">要從中檢索認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffb5-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="dffb5-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="dffb5-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="dffb5-129">要從中檢索認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="dffb5-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dffb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffb5-130">CommonParameters</span></span>
<span data-ttu-id="dffb5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dffb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffb5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dffb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffb5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="dffb5-133">INPUTS</span></span>

### <span data-ttu-id="dffb5-134">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="dffb5-134">System.Guid</span></span>

### <span data-ttu-id="dffb5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="dffb5-135">System.String</span></span>

### <span data-ttu-id="dffb5-136">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dffb5-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="dffb5-137">參數： ServicePrincipalObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dffb5-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="dffb5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dffb5-138">OUTPUTS</span></span>

### <span data-ttu-id="dffb5-139">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="dffb5-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="dffb5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="dffb5-140">NOTES</span></span>

## <span data-ttu-id="dffb5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="dffb5-141">RELATED LINKS</span></span>

[<span data-ttu-id="dffb5-142">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dffb5-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="dffb5-143">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dffb5-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="dffb5-144">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dffb5-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

