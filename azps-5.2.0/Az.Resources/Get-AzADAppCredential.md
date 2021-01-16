---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277364"
---
# <span data-ttu-id="1e6bc-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1e6bc-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="1e6bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6bc-103">檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="1e6bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e6bc-104">SYNTAX</span></span>

### <span data-ttu-id="1e6bc-105">ApplicationObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1e6bc-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6bc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6bc-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6bc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6bc-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6bc-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6bc-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e6bc-109">說明</span><span class="sxs-lookup"><span data-stu-id="1e6bc-109">DESCRIPTION</span></span>
<span data-ttu-id="1e6bc-110">Get-AzADAppCredential Cmdlet 可以用來檢索與應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="1e6bc-111">這個命令會檢索所有認證屬性 (但不會) 與應用程式相關聯的認證值。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="1e6bc-112">示例</span><span class="sxs-lookup"><span data-stu-id="1e6bc-112">EXAMPLES</span></span>

### <span data-ttu-id="1e6bc-113">範例1：依物件識別碼取得應用程式認證</span><span class="sxs-lookup"><span data-stu-id="1e6bc-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="1e6bc-114">傳回與含物件 id ' 1f99cf81-0146-4f4e-beae-2007d0668476」之應用程式相關聯的認證清單。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="1e6bc-115">範例2：透過管道取得應用程式認證</span><span class="sxs-lookup"><span data-stu-id="1e6bc-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="1e6bc-116">取得物件 id 為「1f99cf81-0146-4f4e-beae-2007d0668476」的應用程式，並將其管道至 Get-AzADAppCredential Cmdlet，以列出該應用程式的所有認證。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="1e6bc-117">參數</span><span class="sxs-lookup"><span data-stu-id="1e6bc-117">PARAMETERS</span></span>

### <span data-ttu-id="1e6bc-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1e6bc-118">-ApplicationId</span></span>
<span data-ttu-id="1e6bc-119">要從中檢索認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="1e6bc-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1e6bc-120">-ApplicationObject</span></span>
<span data-ttu-id="1e6bc-121">要從中檢索認證的 application 物件。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="1e6bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6bc-122">-DefaultProfile</span></span>
<span data-ttu-id="1e6bc-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e6bc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e6bc-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1e6bc-124">-DisplayName</span></span>
<span data-ttu-id="1e6bc-125">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-125">The display name of the application.</span></span>

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

### <span data-ttu-id="1e6bc-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1e6bc-126">-ObjectId</span></span>
<span data-ttu-id="1e6bc-127">要從中檢索認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="1e6bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6bc-128">CommonParameters</span></span>
<span data-ttu-id="1e6bc-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6bc-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6bc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1e6bc-131">INPUTS</span></span>

### <span data-ttu-id="1e6bc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1e6bc-132">System.String</span></span>

### <span data-ttu-id="1e6bc-133">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="1e6bc-133">System.Guid</span></span>

### <span data-ttu-id="1e6bc-134">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="1e6bc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1e6bc-135">OUTPUTS</span></span>

### <span data-ttu-id="1e6bc-136">PSADCredential （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1e6bc-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="1e6bc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1e6bc-137">NOTES</span></span>

## <span data-ttu-id="1e6bc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e6bc-138">RELATED LINKS</span></span>

[<span data-ttu-id="1e6bc-139">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1e6bc-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="1e6bc-140">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1e6bc-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="1e6bc-141">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1e6bc-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

