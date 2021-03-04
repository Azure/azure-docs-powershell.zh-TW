---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904346"
---
# <span data-ttu-id="ed364-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ed364-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="ed364-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed364-102">SYNOPSIS</span></span>
<span data-ttu-id="ed364-103">會取回與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="ed364-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="ed364-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed364-104">SYNTAX</span></span>

### <span data-ttu-id="ed364-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ed364-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed364-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed364-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed364-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed364-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed364-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed364-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed364-109">描述</span><span class="sxs-lookup"><span data-stu-id="ed364-109">DESCRIPTION</span></span>
<span data-ttu-id="ed364-110">您可以使用 Get-AzADSpCredential Cmdlet 來取回與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="ed364-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="ed364-111">此命令會從伺服器 (所有認證屬性，但不會) 與服務主體相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="ed364-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="ed364-112">例子</span><span class="sxs-lookup"><span data-stu-id="ed364-112">EXAMPLES</span></span>

### <span data-ttu-id="ed364-113">範例 1 - 按 SPN 列出認證</span><span class="sxs-lookup"><span data-stu-id="ed364-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="ed364-114">會以 SPN ' '，會返回與服務主體相關聯的認證 http://test12345 清單。</span><span class="sxs-lookup"><span data-stu-id="ed364-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="ed364-115">範例 2 - 按物件識別碼列出認證</span><span class="sxs-lookup"><span data-stu-id="ed364-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="ed364-116">會以物件識別碼 "58e28616-99cc-4da4-b705-7672130e1047"，會返回與服務主體相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="ed364-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="ed364-117">範例 3 - 以管道列出認證</span><span class="sxs-lookup"><span data-stu-id="ed364-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="ed364-118">使用物件識別碼 "58e28616-99cc-4da4-b705-7672130e1047" 來獲得服務主體，並管道到 Get-AzADSpCredential Cmdlet，以列出該服務主體的所有認證。</span><span class="sxs-lookup"><span data-stu-id="ed364-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="ed364-119">參數</span><span class="sxs-lookup"><span data-stu-id="ed364-119">PARAMETERS</span></span>

### <span data-ttu-id="ed364-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed364-120">-DefaultProfile</span></span>
<span data-ttu-id="ed364-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ed364-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed364-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed364-122">-DisplayName</span></span>
<span data-ttu-id="ed364-123">服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ed364-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="ed364-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ed364-124">-ObjectId</span></span>
<span data-ttu-id="ed364-125">要從中取回認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed364-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ed364-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed364-126">-ServicePrincipalName</span></span>
<span data-ttu-id="ed364-127">SPN (SPN) 取認證之服務主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed364-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ed364-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="ed364-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="ed364-129">要從中取回認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="ed364-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="ed364-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed364-130">CommonParameters</span></span>
<span data-ttu-id="ed364-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed364-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed364-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed364-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed364-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ed364-133">INPUTS</span></span>

### <span data-ttu-id="ed364-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ed364-134">System.String</span></span>

### <span data-ttu-id="ed364-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ed364-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ed364-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ed364-136">OUTPUTS</span></span>

### <span data-ttu-id="ed364-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ed364-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ed364-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ed364-138">NOTES</span></span>

## <span data-ttu-id="ed364-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed364-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed364-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ed364-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="ed364-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ed364-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="ed364-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ed364-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

