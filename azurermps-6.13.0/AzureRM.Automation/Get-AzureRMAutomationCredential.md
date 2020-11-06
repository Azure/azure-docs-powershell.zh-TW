---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: c92e42f49368e894006da0f7afeb9ffcf7e4a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453932"
---
# <span data-ttu-id="3c648-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3c648-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="3c648-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c648-102">SYNOPSIS</span></span>
<span data-ttu-id="3c648-103">取得自動化認證。</span><span class="sxs-lookup"><span data-stu-id="3c648-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c648-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c648-104">SYNTAX</span></span>

### <span data-ttu-id="3c648-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="3c648-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c648-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3c648-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c648-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c648-107">DESCRIPTION</span></span>
<span data-ttu-id="3c648-108">**AzureRmAutomationCredential** Cmdlet 會取得一或多個 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="3c648-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="3c648-109">根據預設，會傳回所有認證。</span><span class="sxs-lookup"><span data-stu-id="3c648-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="3c648-110">指定認證的名稱以取得特定認證。</span><span class="sxs-lookup"><span data-stu-id="3c648-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="3c648-111">為安全起見，這個 Cmdlet 不會傳回認證密碼。</span><span class="sxs-lookup"><span data-stu-id="3c648-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="3c648-112">示例</span><span class="sxs-lookup"><span data-stu-id="3c648-112">EXAMPLES</span></span>

### <span data-ttu-id="3c648-113">範例1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="3c648-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3c648-114">這個命令會針對自動化帳戶（名為 Contoso17）中的所有認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3c648-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3c648-115">範例2：取得認證</span><span class="sxs-lookup"><span data-stu-id="3c648-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="3c648-116">這個命令會在名為 Contoso17 的自動化帳戶中，為名為 ContosoCredential 的認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3c648-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3c648-117">參數</span><span class="sxs-lookup"><span data-stu-id="3c648-117">PARAMETERS</span></span>

### <span data-ttu-id="3c648-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3c648-118">-AutomationAccountName</span></span>
<span data-ttu-id="3c648-119">指定此 Cmdlet 為其檢索認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3c648-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c648-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c648-120">-DefaultProfile</span></span>
<span data-ttu-id="3c648-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3c648-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c648-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c648-122">-Name</span></span>
<span data-ttu-id="3c648-123">指定要取得認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c648-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c648-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c648-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c648-125">指定此 Cmdlet 為其檢索認證的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3c648-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c648-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c648-126">CommonParameters</span></span>
<span data-ttu-id="3c648-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c648-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c648-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c648-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c648-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3c648-129">INPUTS</span></span>

### <span data-ttu-id="3c648-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3c648-130">System.String</span></span>

## <span data-ttu-id="3c648-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3c648-131">OUTPUTS</span></span>

### <span data-ttu-id="3c648-132">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c648-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="3c648-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3c648-133">NOTES</span></span>

## <span data-ttu-id="3c648-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c648-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c648-135">新-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3c648-135">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="3c648-136">移除-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3c648-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="3c648-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3c648-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


