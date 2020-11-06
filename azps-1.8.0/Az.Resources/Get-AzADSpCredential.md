---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 5307e070f8c568473e1ce35f1183517cd3def05c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620895"
---
# <span data-ttu-id="e966d-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e966d-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="e966d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e966d-102">SYNOPSIS</span></span>
<span data-ttu-id="e966d-103">檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="e966d-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="e966d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e966d-104">SYNTAX</span></span>

### <span data-ttu-id="e966d-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e966d-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e966d-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e966d-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e966d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e966d-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e966d-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e966d-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e966d-109">說明</span><span class="sxs-lookup"><span data-stu-id="e966d-109">DESCRIPTION</span></span>
<span data-ttu-id="e966d-110">Get-AzADSpCredential Cmdlet 可以用來檢索與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="e966d-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="e966d-111">這個命令會檢索所有認證屬性 (但不會) 與服務主體相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="e966d-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="e966d-112">示例</span><span class="sxs-lookup"><span data-stu-id="e966d-112">EXAMPLES</span></span>

### <span data-ttu-id="e966d-113">範例 1-依 SPN 列出認證</span><span class="sxs-lookup"><span data-stu-id="e966d-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="e966d-114">使用 SPN "" 傳回與服務主體相關聯的認證清單 http://test12345 。</span><span class="sxs-lookup"><span data-stu-id="e966d-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="e966d-115">範例 2-依物件識別碼列出認證</span><span class="sxs-lookup"><span data-stu-id="e966d-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="e966d-116">使用物件 id "58e28616-99cc-4da4-b705-7672130e1047" 傳回與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="e966d-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="e966d-117">範例 3-依管道列出認證</span><span class="sxs-lookup"><span data-stu-id="e966d-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="e966d-118">取得物件識別碼為 "58e28616-99cc-4da4-b705-7672130e1047" 的服務主體，並將其管道至 Get-AzADSpCredential Cmdlet，以列出該服務主體的所有認證。</span><span class="sxs-lookup"><span data-stu-id="e966d-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="e966d-119">參數</span><span class="sxs-lookup"><span data-stu-id="e966d-119">PARAMETERS</span></span>

### <span data-ttu-id="e966d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e966d-120">-DefaultProfile</span></span>
<span data-ttu-id="e966d-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e966d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e966d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e966d-122">-DisplayName</span></span>
<span data-ttu-id="e966d-123">服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e966d-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="e966d-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e966d-124">-ObjectId</span></span>
<span data-ttu-id="e966d-125">要從中檢索認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e966d-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e966d-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e966d-126">-ServicePrincipalName</span></span>
<span data-ttu-id="e966d-127">要從中檢索認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e966d-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e966d-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="e966d-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="e966d-129">要從中檢索認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="e966d-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e966d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e966d-130">CommonParameters</span></span>
<span data-ttu-id="e966d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e966d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e966d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e966d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e966d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e966d-133">INPUTS</span></span>

### <span data-ttu-id="e966d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e966d-134">System.String</span></span>

### <span data-ttu-id="e966d-135">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e966d-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e966d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e966d-136">OUTPUTS</span></span>

### <span data-ttu-id="e966d-137">PSADCredential （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e966d-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e966d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e966d-138">NOTES</span></span>

## <span data-ttu-id="e966d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e966d-139">RELATED LINKS</span></span>

[<span data-ttu-id="e966d-140">新-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e966d-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="e966d-141">移除-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e966d-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="e966d-142">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e966d-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

