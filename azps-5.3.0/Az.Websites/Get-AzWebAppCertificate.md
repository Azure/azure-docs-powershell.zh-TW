---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436025"
---
# <span data-ttu-id="b2363-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="b2363-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="b2363-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2363-102">SYNOPSIS</span></span>
<span data-ttu-id="b2363-103">取得 Azure Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="b2363-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="b2363-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2363-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2363-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2363-105">DESCRIPTION</span></span>
<span data-ttu-id="b2363-106">**AzWebAppCertificate** Cmdlet 會取得與指定資源群組相關聯之 Azure Web App 憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b2363-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="b2363-107">如果您知道憑證指紋，您也可以使用這個 Cmdlet 來取得指定憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b2363-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="b2363-108">示例</span><span class="sxs-lookup"><span data-stu-id="b2363-108">EXAMPLES</span></span>

### <span data-ttu-id="b2363-109">範例1：取得資源群組中的 Web 應用程式憑證</span><span class="sxs-lookup"><span data-stu-id="b2363-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="b2363-110">這個命令會傳回與資源群組 ContosoResourceGroup 相關聯的上傳 Web App 憑證資訊。</span><span class="sxs-lookup"><span data-stu-id="b2363-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2363-111">範例2：取得指定的 web 應用程式憑證</span><span class="sxs-lookup"><span data-stu-id="b2363-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="b2363-112">這個命令會取得指紋 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 的 ContosoResourceGroup Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="b2363-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="b2363-113">參數</span><span class="sxs-lookup"><span data-stu-id="b2363-113">PARAMETERS</span></span>

### <span data-ttu-id="b2363-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2363-114">-DefaultProfile</span></span>
<span data-ttu-id="b2363-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2363-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2363-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2363-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2363-117">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2363-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="b2363-118">-指紋</span><span class="sxs-lookup"><span data-stu-id="b2363-118">-Thumbprint</span></span>
<span data-ttu-id="b2363-119">指定憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2363-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="b2363-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2363-120">CommonParameters</span></span>
<span data-ttu-id="b2363-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2363-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2363-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2363-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2363-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b2363-123">INPUTS</span></span>

### <span data-ttu-id="b2363-124">所有</span><span class="sxs-lookup"><span data-stu-id="b2363-124">None</span></span>

## <span data-ttu-id="b2363-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b2363-125">OUTPUTS</span></span>

### <span data-ttu-id="b2363-126">WebApps WebApp. PSCertificate （）</span><span class="sxs-lookup"><span data-stu-id="b2363-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="b2363-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b2363-127">NOTES</span></span>

## <span data-ttu-id="b2363-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2363-128">RELATED LINKS</span></span>

[<span data-ttu-id="b2363-129">AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b2363-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


