---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: c96fceb331a2b33528b47506e928ea78cfc793d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907541"
---
# <span data-ttu-id="a61f2-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a61f2-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="a61f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a61f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a61f2-103">會取回與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="a61f2-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="a61f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a61f2-104">SYNTAX</span></span>

### <span data-ttu-id="a61f2-105">ApplicationObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a61f2-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a61f2-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a61f2-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a61f2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a61f2-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a61f2-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a61f2-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a61f2-109">描述</span><span class="sxs-lookup"><span data-stu-id="a61f2-109">DESCRIPTION</span></span>
<span data-ttu-id="a61f2-110">您可以使用Get-AzADAppCredential Cmdlet 來取回與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="a61f2-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="a61f2-111">此命令會從應用程式 (所有認證屬性，) 與應用程式關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="a61f2-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="a61f2-112">例子</span><span class="sxs-lookup"><span data-stu-id="a61f2-112">EXAMPLES</span></span>

### <span data-ttu-id="a61f2-113">範例 1：根據物件識別碼取得應用程式認證</span><span class="sxs-lookup"><span data-stu-id="a61f2-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="a61f2-114">會返回與具有物件識別碼 '1f99cf81-0146-4f4e-beae-2007d0668476'的應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="a61f2-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="a61f2-115">範例 2：使用管道取得應用程式認證</span><span class="sxs-lookup"><span data-stu-id="a61f2-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="a61f2-116">使用物件識別碼為 "1f99cf81-0146-4f4e-beae-2007d0668476" 的應用程式，並管道到 Get-AzADAppCredential Cmdlet，以列出該應用程式的所有認證。</span><span class="sxs-lookup"><span data-stu-id="a61f2-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="a61f2-117">參數</span><span class="sxs-lookup"><span data-stu-id="a61f2-117">PARAMETERS</span></span>

### <span data-ttu-id="a61f2-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a61f2-118">-ApplicationId</span></span>
<span data-ttu-id="a61f2-119">要從中取回認證之應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a61f2-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a61f2-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a61f2-120">-ApplicationObject</span></span>
<span data-ttu-id="a61f2-121">要從中取回認證的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="a61f2-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a61f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61f2-122">-DefaultProfile</span></span>
<span data-ttu-id="a61f2-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a61f2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a61f2-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a61f2-124">-DisplayName</span></span>
<span data-ttu-id="a61f2-125">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a61f2-125">The display name of the application.</span></span>

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

### <span data-ttu-id="a61f2-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a61f2-126">-ObjectId</span></span>
<span data-ttu-id="a61f2-127">要從中取回認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a61f2-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="a61f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61f2-128">CommonParameters</span></span>
<span data-ttu-id="a61f2-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a61f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61f2-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a61f2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61f2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a61f2-131">INPUTS</span></span>

### <span data-ttu-id="a61f2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a61f2-132">System.String</span></span>

### <span data-ttu-id="a61f2-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a61f2-133">System.Guid</span></span>

### <span data-ttu-id="a61f2-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a61f2-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a61f2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a61f2-135">OUTPUTS</span></span>

### <span data-ttu-id="a61f2-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a61f2-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="a61f2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a61f2-137">NOTES</span></span>

## <span data-ttu-id="a61f2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a61f2-138">RELATED LINKS</span></span>

[<span data-ttu-id="a61f2-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a61f2-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a61f2-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a61f2-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="a61f2-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a61f2-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

