---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: 12603400c3d1f29eaf77d9a279d7510e08b9fe5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912517"
---
# <span data-ttu-id="23db3-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="23db3-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="23db3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23db3-102">SYNOPSIS</span></span>
<span data-ttu-id="23db3-103">獲得 Azure Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="23db3-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="23db3-104">語法</span><span class="sxs-lookup"><span data-stu-id="23db3-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23db3-105">描述</span><span class="sxs-lookup"><span data-stu-id="23db3-105">DESCRIPTION</span></span>
<span data-ttu-id="23db3-106">**Get-AzWebAppCertificate** Cmdlet 會取得與指定資源群組相關聯的 Azure Web App 憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="23db3-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="23db3-107">如果您知道憑證指紋，您也可以使用此 Cmdlet 取得指定憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="23db3-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="23db3-108">例子</span><span class="sxs-lookup"><span data-stu-id="23db3-108">EXAMPLES</span></span>

### <span data-ttu-id="23db3-109">範例 1：在資源群組中取得 Web App 憑證</span><span class="sxs-lookup"><span data-stu-id="23db3-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="23db3-110">此命令會返回與資源群組 ContosoResourceGroup 相關聯的已上傳 Web App 憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="23db3-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="23db3-111">範例 2：取得指定的 Web App 憑證</span><span class="sxs-lookup"><span data-stu-id="23db3-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="23db3-112">此命令會以指紋 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 獲得 ContosoResourceGroup Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="23db3-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="23db3-113">參數</span><span class="sxs-lookup"><span data-stu-id="23db3-113">PARAMETERS</span></span>

### <span data-ttu-id="23db3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23db3-114">-DefaultProfile</span></span>
<span data-ttu-id="23db3-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23db3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23db3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23db3-116">-ResourceGroupName</span></span>
<span data-ttu-id="23db3-117">指定憑證指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="23db3-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23db3-118">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="23db3-118">-Thumbprint</span></span>
<span data-ttu-id="23db3-119">指定憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="23db3-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23db3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23db3-120">CommonParameters</span></span>
<span data-ttu-id="23db3-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23db3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23db3-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="23db3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23db3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23db3-123">INPUTS</span></span>

### <span data-ttu-id="23db3-124">沒有</span><span class="sxs-lookup"><span data-stu-id="23db3-124">None</span></span>

## <span data-ttu-id="23db3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="23db3-125">OUTPUTS</span></span>

### <span data-ttu-id="23db3-126">Microsoft.Azure.Commands.WebApps.models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="23db3-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="23db3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="23db3-127">NOTES</span></span>

## <span data-ttu-id="23db3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="23db3-128">RELATED LINKS</span></span>

[<span data-ttu-id="23db3-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="23db3-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


