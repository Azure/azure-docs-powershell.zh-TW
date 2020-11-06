---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: e2aaa6ed6e66e61f8d62f1235ff8e2a8ff9f65e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445916"
---
# <span data-ttu-id="a0fab-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a0fab-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="a0fab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0fab-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fab-103">取得 Azure Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="a0fab-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0fab-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0fab-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0fab-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0fab-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fab-106">**AzureRmWebAppCertificate** Cmdlet 會取得與指定資源群組相關聯之 Azure Web App 憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0fab-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="a0fab-107">如果您知道憑證指紋，您也可以使用這個 Cmdlet 來取得指定憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0fab-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="a0fab-108">示例</span><span class="sxs-lookup"><span data-stu-id="a0fab-108">EXAMPLES</span></span>

### <span data-ttu-id="a0fab-109">範例1：取得資源群組中的 Web 應用程式憑證</span><span class="sxs-lookup"><span data-stu-id="a0fab-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a0fab-110">這個命令會傳回與資源群組 ContosoResourceGroup 相關聯的上傳 Web App 憑證資訊。</span><span class="sxs-lookup"><span data-stu-id="a0fab-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="a0fab-111">範例2：取得指定的 web 應用程式憑證</span><span class="sxs-lookup"><span data-stu-id="a0fab-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a0fab-112">這個命令會取得指紋 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 的 ContosoResourceGroup Web App 憑證。</span><span class="sxs-lookup"><span data-stu-id="a0fab-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="a0fab-113">參數</span><span class="sxs-lookup"><span data-stu-id="a0fab-113">PARAMETERS</span></span>

### <span data-ttu-id="a0fab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fab-114">-DefaultProfile</span></span>
<span data-ttu-id="a0fab-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0fab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0fab-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fab-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0fab-117">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0fab-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fab-118">-指紋</span><span class="sxs-lookup"><span data-stu-id="a0fab-118">-Thumbprint</span></span>
<span data-ttu-id="a0fab-119">指定憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0fab-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fab-120">CommonParameters</span></span>
<span data-ttu-id="a0fab-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0fab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fab-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0fab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fab-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a0fab-123">INPUTS</span></span>

### <span data-ttu-id="a0fab-124">所有</span><span class="sxs-lookup"><span data-stu-id="a0fab-124">None</span></span>
<span data-ttu-id="a0fab-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a0fab-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0fab-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a0fab-126">OUTPUTS</span></span>

## <span data-ttu-id="a0fab-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a0fab-127">NOTES</span></span>

## <span data-ttu-id="a0fab-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0fab-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0fab-129">AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a0fab-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


