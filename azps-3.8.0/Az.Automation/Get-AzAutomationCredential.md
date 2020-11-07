---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958655"
---
# <span data-ttu-id="edf87-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="edf87-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="edf87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edf87-102">SYNOPSIS</span></span>
<span data-ttu-id="edf87-103">取得自動化認證。</span><span class="sxs-lookup"><span data-stu-id="edf87-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="edf87-104">句法</span><span class="sxs-lookup"><span data-stu-id="edf87-104">SYNTAX</span></span>

### <span data-ttu-id="edf87-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="edf87-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edf87-106">ByName</span><span class="sxs-lookup"><span data-stu-id="edf87-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edf87-107">說明</span><span class="sxs-lookup"><span data-stu-id="edf87-107">DESCRIPTION</span></span>
<span data-ttu-id="edf87-108">**AzAutomationCredential** Cmdlet 會取得一或多個 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="edf87-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="edf87-109">根據預設，會傳回所有認證。</span><span class="sxs-lookup"><span data-stu-id="edf87-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="edf87-110">指定認證的名稱以取得特定認證。</span><span class="sxs-lookup"><span data-stu-id="edf87-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="edf87-111">為安全起見，這個 Cmdlet 不會傳回認證密碼。</span><span class="sxs-lookup"><span data-stu-id="edf87-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="edf87-112">示例</span><span class="sxs-lookup"><span data-stu-id="edf87-112">EXAMPLES</span></span>

### <span data-ttu-id="edf87-113">範例1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="edf87-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="edf87-114">這個命令會針對自動化帳戶（名為 Contoso17）中的所有認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="edf87-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="edf87-115">範例2：取得認證</span><span class="sxs-lookup"><span data-stu-id="edf87-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="edf87-116">這個命令會在名為 Contoso17 的自動化帳戶中，為名為 ContosoCredential 的認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="edf87-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="edf87-117">參數</span><span class="sxs-lookup"><span data-stu-id="edf87-117">PARAMETERS</span></span>

### <span data-ttu-id="edf87-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="edf87-118">-AutomationAccountName</span></span>
<span data-ttu-id="edf87-119">指定此 Cmdlet 為其檢索認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="edf87-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="edf87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf87-120">-DefaultProfile</span></span>
<span data-ttu-id="edf87-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="edf87-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edf87-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="edf87-122">-Name</span></span>
<span data-ttu-id="edf87-123">指定要取得認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="edf87-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="edf87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf87-124">-ResourceGroupName</span></span>
<span data-ttu-id="edf87-125">指定此 Cmdlet 為其檢索認證的資源群組。</span><span class="sxs-lookup"><span data-stu-id="edf87-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="edf87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf87-126">CommonParameters</span></span>
<span data-ttu-id="edf87-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edf87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf87-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edf87-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf87-129">輸入</span><span class="sxs-lookup"><span data-stu-id="edf87-129">INPUTS</span></span>

### <span data-ttu-id="edf87-130">System.object</span><span class="sxs-lookup"><span data-stu-id="edf87-130">System.String</span></span>

## <span data-ttu-id="edf87-131">輸出</span><span class="sxs-lookup"><span data-stu-id="edf87-131">OUTPUTS</span></span>

### <span data-ttu-id="edf87-132">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edf87-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="edf87-133">筆記</span><span class="sxs-lookup"><span data-stu-id="edf87-133">NOTES</span></span>

## <span data-ttu-id="edf87-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="edf87-134">RELATED LINKS</span></span>

[<span data-ttu-id="edf87-135">新-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="edf87-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="edf87-136">移除-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="edf87-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="edf87-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="edf87-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


